# SetPartDataID

## Description
Set a numeric value for this part instance represented by the specified sub-object.<BR>
The sub-object must be an object that was tagged as a part.

```pascal
PROCEDURE SetPartDataID(
				objectHandle : HANDLE;
				dataID       : LONGINT);
```

```python
def vs.SetPartDataID(objectHandle, dataID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|The sub-object handle.|
|dataID|LONGINT|The numeric value assigned to the part.|

## Examples
```pascal
SetPartDataID(objectHandle, 1);
```
```python
import vs

# Set a numeric value for this part instance represented by the specified
# sub-object.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
dataID = 1

vs.SetPartDataID(objectHandle, dataID)
```

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
