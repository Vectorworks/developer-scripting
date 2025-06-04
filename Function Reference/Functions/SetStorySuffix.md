# SetStorySuffix

## Description
Sets the suffix of the indicated Story. Returns whether the suffix was successfully set. If the suffix is already used by another Story, then the change in suffix will be prevented.

```pascal
FUNCTION SetStorySuffix(
				story  : HANDLE;
				suffix : STRING): BOOLEAN;
```

```python
def vs.SetStorySuffix(story, suffix):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|story|HANDLE|The story whose suffix is being set.|
|suffix|STRING|The new value of the suffix of the indicated Story.|

## See Also
VS Functions:
[GetStorySuffix](GetStorySuffix.md) 
| [SetStoryElevation](SetStoryElevation.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
