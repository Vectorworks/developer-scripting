# GetComponentWidth

## Description
Gets the width of a component in an object.

```pascal
FUNCTION GetComponentWidth(
				obj            : HANDLE;
				componentIndex : INTEGER;
				VAR width      : REAL): BOOLEAN;
```

```python
def vs.GetComponentWidth(obj, componentIndex):
    return (BOOLEAN, width)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|width|REAL|Returns the width of the component.|

## Examples
```pascal
BEGIN
	bIsUni := TRUE;
	curCmpWidth := GetComponentWidth( 1 );
	FOR cnt := 2 to componentCnt DO BEGIN
		IF curCmpWidth <> GetComponentWidth( cnt ) THEN bIsUni := FALSE;
	END;

theWidth := 0;
numComponents := GetObjectVariableInt(wallHandle, 199);
if numComponents > 0 then BEGIN
	for cnt := 1 to numComponents do BEGIN
		if GetComponentWidth(wallHandle, cnt, componentWidth) then BEGIN
			theWidth := theWidth + componentWidth;
		END;

BEGIN
result := GetComponentWidth( extStyle_h, cnt, currTMPOffset );
if cnt = coreComponentIndex THEN
	BEGIN
	offset := offset + currTMPOffset;
	cnt := numberOfComponents;
```
```python
import vs

# Gets the width of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, width = vs.GetComponentWidth(obj, componentIndex)
vs.Message('GetComponentWidth returned: ' + str((ok, width)))
```

## See Also
VS Functions:
[SetComponentWidth](SetComponentWidth.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
