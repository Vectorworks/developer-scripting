# GetPartTypeName

## Description
Return the part type for the specified sub-object.<BR>
The sub-object must be an object that was tagged as a part.

```pascal
FUNCTION GetPartTypeName(objectHandle : HANDLE): STRING;
```

```python
def vs.GetPartTypeName(objectHandle):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|The sub-object handle.|

## Examples
```pascal
resultStr := GetPartTypeName(objectHandle);
```
```python
import vs

# Return the part type for the specified sub-object.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

name = vs.GetPartTypeName(objectHandle)
vs.Message('GetPartTypeName returned: ' + str(name))
```

## See Also
VS Functions:
[TagSubObjectAsPart](TagSubObjectAsPart.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
