# HExtrude

## Description
Creates an extrude object from the specified object.

```pascal
FUNCTION HExtrude(
				objectH : HANDLE;
				bottom  : REAL;
				top     : REAL): HANDLE;
```

```python
def vs.HExtrude(objectH, bottom, top):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectH|HANDLE|The profile to be extruded.|
|bottom|REAL|The z height of the bottom of the extrude.|
|top|REAL|The z height of the top of the extrude.|

## Remarks
hExtrude does not work inside PIOs. Uses BeginXtrd and EndXtrd instead. 
If you need to extrude a Symbol inside a PIO use following workaround (idea by heiner schmalbach). This code shows the principle behind the idea:
```pascal
PioInfoOK := GetCustomObjectInfo ( PIOName, hPIO, hRecord, hWall);
HandleSymbol2D := GetObject(mNameSymbol);
If HandleSymbol2D = nil then SymbolError := true
else
Begin
Symbol(mNameSymbol,0,0,0);
hSymbol := lNewObj;
SymbolToGroup (hSymbol, 2);
hPoly := fIn3D(fIn3D(fIn3D(hPIO))); 
{in this case: first object in symbol is a polygone. You have to find 
your own way to select the right object.}
BeginXtrd(0,200);  {create a dummy extrude}
Rect(0,0,200,200);
EndXtrd;
hSymbol3D := lNewObj;
SettingParentOK := SetParent(hPoly,hSchiene3D);  
{Set the 3D extrude as parent of your symbol polygone}

hDummy := fIn3D(hSymbol3D); {Select the "dummy rectangle"}
DelObject(hDummy);  {delete the dummy rectangle}
End;
```

HExtrude doesn't work in any group-like container. Below another possibility for creating a 3D object while preserving the original 2D object:
```pascal
{ ***************************************** }
{ Orso.B.Schmid, creates an extrude from a HANDLE h, 
preserving the original h. Returns a handle to the extrude }
FUNCTION Create3Dobj(h: HANDLE; z, dZ: REAL): HANDLE;
BEGIN
IF h &lt;&gt; NIL THEN BEGIN
BeginXtrd(z, dZ);
Line(1, 1); 
{ just draw something for creating an extrude container }
EndXtrd;

DelObject(FIn3D(GetParent(CreateDuplicateObject(h, LNewObj))));
{ places a copy of h in the extrude and deletes the line }

Create3Dobj := LNewObj;
END;
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
