# SetCompAltSecFill

## Description
Sets the alternate section fill of a component in an object.

```pascal
FUNCTION SetCompAltSecFill(
				object               : HANDLE;
				componentIndex       : INTEGER;
				alternateSectionFill : LONGINT): BOOLEAN;
```

```python
def vs.SetCompAltSecFill(object, componentIndex, alternateSectionFill):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|alternateSectionFill|LONGINT|The alternate section fill of the component.|

## See Also
VS Functions:
[GetCompAltSecFill](GetCompAltSecFill.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
