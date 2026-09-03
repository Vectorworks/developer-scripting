# IsObjectTaggedAsPart

## Description
Determine if the specified sub-object is tagged as a part.

```pascal
FUNCTION IsObjectTaggedAsPart(objectHandle : HANDLE): BOOLEAN;
```

```python
def vs.IsObjectTaggedAsPart(objectHandle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|The sub-object handle.|

## Examples
```pascal
resultOK := IsObjectTaggedAsPart(objectHandle);
```
```python
import vs

# Determine if the specified sub-object is tagged as a part.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.IsObjectTaggedAsPart(objectHandle)
if ok:
    vs.Message('IsObjectTaggedAsPart succeeded')
else:
    vs.Message('IsObjectTaggedAsPart failed')
```

## See Also
VS Functions:
[TagSubObjectAsPart](TagSubObjectAsPart.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
