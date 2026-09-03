# GetSymbolType

## Description
Determines the type of the specified symbol instance.  The return values are:
0 - 2D Only
1 - 3D Only
2 - Hybrid

```pascal
FUNCTION GetSymbolType(objectHandle : HANDLE): INTEGER;
```

```python
def vs.GetSymbolType(objectHandle):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to a symbol instance.|

## Examples
```pascal
symType := GetSymbolType(GetObject(gSymbolName)); { type is -1 when handle is NIL }

		END;
END;
fuzz := .1";
hght := pBaseZ;
OK2Move3D := (GetSymbolType(GetObject(symbolName)) > 0);
EnableParameter(objHand, 'baseZ', OK2Move3D);
EnableParameter(objHand, 'rise', OK2Move3D);
subTotal := 0;
foc_pt.x := pControlPoint01X;

IF (LecHand <> NIL) & (GetSymbolType(LecSymHand) <> 0) & (GetProjection(ActLayer) = 6) THEN
	BEGIN
	TotalHeight := 0;
	GetBBox(LecHand,p1x,p1y,p2x,p2y);
	p1x:=p1x-p2x+1";
	p1y:=p1y-p2y+1";
	GetSymLoc(LecHand,x,y);
```
```python
import vs

# Determines the type of the specified symbol instance.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetSymbolType(objectHandle)
vs.Message('GetSymbolType returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
