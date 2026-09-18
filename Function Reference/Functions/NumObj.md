# NumObj

## Description
Function NumObj returns the number of objects on the referenced layer.

```pascal
FUNCTION NumObj(h : HANDLE): LONGINT;
```

```python
def vs.NumObj(h):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to layer.|

## Examples
```pascal
BEGIN
IF kDebug THEN Writeln(GetLName(hTempLayer),' has ',NumObj(hTempLayer),' Objects');
hTempLayer1 := hTempLayer;
hTempLayer := NextLayer(hTempLayer);
IF (GetObjectVariableInt(hTempLayer1,154) = 1) & (NumObj(hTempLayer1) = 0) THEN
	BEGIN

BEGIN
	gSheetInfo [index].SheetName		:= sheetName;
	gSheetInfo [index].SheetType		:= sheetType;
	gSheetInfo [index].Instance		:= 1;
	gSheetInfo [index].HasBorder		:= (NumObj (layerH) > 0);
	gSheetInfo [index].BorderType		:= gNuTitleBlockType;
	gSheetInfo [index].HasSheetChanged	:= FALSE;
	gSheetInfo [index].HasBorderChanged	:= FALSE;
	gSheetInfo [index].NewBorderType	:= gNuTitleBlockType;

IF NumObj (layerH) = 0 THEN
BEGIN
	layerToDelete := layerH;
	layerH := NextObj (layerH);
	DelObject (layerToDelete);
END
```
```python
import vs

# Function NumObj returns the number of objects on the referenced layer.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

count = vs.NumObj(h)
vs.Message('NumObj returned: ' + str(count))
```

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
