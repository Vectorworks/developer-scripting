# FIn3D

## Description
Function FIn3D returns a handle to the first component object in the referenced 3D object definition.

```pascal
FUNCTION FIn3D(objectHd : HANDLE): HANDLE;
```

```python
def vs.FIn3D(objectHd):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to object.|

## Examples
```pascal
if ( GetType(h) = 68 ) then BEGIN
	h1 := WallFootPrint(h);
	ok := TRUE;
END else if (GetType(h) = 71) & (GetObjectVariableInt(h, 172) = 3) then BEGIN
	h1 := HDuplicate(FIn3D(h), 0, 0);
	ok := TRUE;
END;

BEGIN
	curObject := FIn3D(wallHandle);
	while ((curObject <> NIL) & (GetType(curObject) <> 6)) DO curObject := NextObj(curObject);
	IF (curObject <> NIL) THEN HCenter(curObject, xCenter, yCenter);
END;

{texture model}
textureIndex := GetTextureRef(gMyHand, 0, FALSE); {Get the texture index assigned to the PIO.}
ForEachObjectInList(AssignTexures, 0, 2, FIn3D(gMyHand)); {Apply it to any untextured objects in the PIO.}
```
```python
# Get the texture index assigned to the PIO.
pIOTexIndex = vs.GetTextureRefN( objHand, 0, 0 False )
# Apply it to any untextured objects in the PIO.
vs.ForEachObjectInList( AssignTex, 0, 2, vs.FIn3D( objHand ) )
```

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
