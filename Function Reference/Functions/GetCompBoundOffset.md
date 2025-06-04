# GetCompBoundOffset

## Description
Gets the bound offset of a component in an object.

```pascal
FUNCTION GetCompBoundOffset(
				object          : HANDLE;
				componentIndex  : INTEGER;
				VAR boundOffset : REAL): BOOLEAN;
```

```python
def vs.GetCompBoundOffset(object, componentIndex):
    return (BOOLEAN, boundOffset)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|boundOffset|REAL|Returns the bound offset of the component.|

## See Also
VS Functions:
[SetCompBoundOffset](SetCompBoundOffset.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
