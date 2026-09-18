# GetLW

## Description
Function GetLW returns the line weight of the referenced object. The value returned represents the width in mils.

```pascal
FUNCTION GetLW(h : HANDLE): INTEGER;
```

```python
def vs.GetLW(h):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Criteria searching by lineweight works differently. An object with a lineweight by class can be found with this: 
```SelectObj((LW<.0000000000002));```
Then you can use GetLW to determine the actual lineweight.

[[User:Orso.b.schmid| orso]]: (1 mil = 1/1000 in)

## Examples
#### VectorScript ####
```pascal
PROCEDURE GetLWExample;
VAR
    x, y : REAL;
    h : HANDLE;
BEGIN
    GetPt(x, y);
    h := PickObject(x, y);

    IF h <> NIL THEN
        Message(GetLW(h));
END;
RUN(GetLWExample);
```
#### Python ####
```python
def PickPointCallback(pt):
	h = vs.PickObject(pt[0], pt[1])
	if h != None:
		vs.Message(vs.GetLW(h))
	

def GetLWExample():
	vs.GetPt( PickPointCallback )
    
GetLWExample()
```

```pascal
BEGIN
	GetPenFore(gLine,R,G,B);
	thk := getLW(gLine);
END;

BEGIN
	GetPenFore (gWallHand,r,g,b);
	PenFore (r,g,b);
	Pensize (GetLW (gWallHand));
	PenPatN (GetLSN (gWallHand));
	GetFillBack (gWallHand,r,g,b);
	FillBack (r,g,b);
END;

{====================== Set Attributes ======================}
{set Callout Line style from the TextNote Group LS}
if arcLineH <> NIl then SetLSN( CNH, GetLSN( arcLineH ) ) ELSE SetLSN( CNH, GetLSN( arrowLineH ) );
{set Callout Line thickness from the TextNote Group LW}
if arcLineH <> NIl then SetLW( CNH, GetLW( arcLineH ) ) ELSE SetLW( CNH, GetLW( arrowLineH ) );
{set Callout PenFore from the TextNote text block PenFore}
GetPenFore( textFoundH, red, green, blue );
SetPenFore( CNH, red, green, blue );
{set Callout PenFore from the TextNote Group PenFore
```
```python
if vs.IsLWByClass(gObjHandle):
	vs.SetLWByClass(hObjectHand)
else:
	nLineWeight = vs.GetLW ( gObjHandle )
	vs.SetLW( hObjectHand, nLineWeight )

if not vs.IsLWByClass( objHand ):
	penSize	= vs.GetLW( objHand )
	vs.PenSize( penSize )

if setLineWeight:
	vs.SetLW(objH, vs.GetLW(parentH))
```

## Version
Availability: from All Versions

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
