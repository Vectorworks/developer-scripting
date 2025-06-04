# SetCompBoundOffset

## Description
Sets the bound offset of a component in an object.

```pascal
FUNCTION SetCompBoundOffset(
				object         : HANDLE;
				componentIndex : INTEGER;
				boundOffset    : REAL): BOOLEAN;
```

```python
def vs.SetCompBoundOffset(object, componentIndex, boundOffset):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|boundOffset|REAL|The bound offset of the component.|

## See Also
VS Functions:
[GetCompBoundOffset](GetCompBoundOffset.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
