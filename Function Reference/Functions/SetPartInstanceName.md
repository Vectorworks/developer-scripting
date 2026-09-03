# SetPartInstanceName

## Description
Set a unique part name for this part instance represented by the specified sub-object.<BR>
The sub-object must be an object that was tagged as a part.

```pascal
PROCEDURE SetPartInstanceName(
				objectHandle       : HANDLE;
				uniqueInstanceName : STRING);
```

```python
def vs.SetPartInstanceName(objectHandle, uniqueInstanceName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|The sub-object handle.|
|uniqueInstanceName|STRING|The unique part name to be assigned assigned to this part instance. The name must be unique for all instances of the part within an object.|

## Examples
```pascal
SetPartInstanceName(objectHandle, 'Example');
```
```python
import vs

# Set a unique part name for this part instance represented by the specified
# sub-object.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
uniqueInstanceName = 'Example'

vs.SetPartInstanceName(objectHandle, uniqueInstanceName)
```

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
