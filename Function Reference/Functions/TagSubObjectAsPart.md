# TagSubObjectAsPart

## Description
Tag the specified sub-object as part.

```pascal
PROCEDURE TagSubObjectAsPart(
				objectHandle : HANDLE;
				partTypeName : STRING;
				dataID       : LONGINT;
				instanceName : STRING);
```

```python
def vs.TagSubObjectAsPart(objectHandle, partTypeName, dataID, instanceName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|The sub-object handle|
|partTypeName|STRING|The name of the part type.|
|dataID|LONGINT|A numeric value assigned to the part (optional)|
|instanceName|STRING|A unique name for this specific part instance (optional). If specified, the name must be unique for all instances of the part within an object.|

## Examples
```pascal
BEGIN
	IF asArchitectural THEN TagSubObjectAsPart(partH, kArchitecturalPart,0,'')
	ELSE TagSubObjectAsPart(partH, kStructuralPart,0,'');

BEGIN
	TagSubObjectAsPart( gFloorH, 'Massing Model Floor', i+1, concat('Floor', i+1) );{'Massing Model Floor'-should be the same as in Plug-in manager/Edit Definition/Subparts}
	SetFloorDataRec( gFloorH, i+1,tmpFlString, tmpClassStr, tmpHeightStr, gFlArea );
END;
```
```python
import vs

# Tag the specified sub-object as part.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
partTypeName = 'Example'
dataID = 1
instanceName = 'Example'

vs.TagSubObjectAsPart(objectHandle, partTypeName, dataID, instanceName)
```

## See Also
VS Functions:
[IsObjectTaggedAsPart](IsObjectTaggedAsPart.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
