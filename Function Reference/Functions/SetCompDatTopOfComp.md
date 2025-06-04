# SetCompDatTopOfComp

## Description
Sets the datum is top of component flag of a component in an object.

```pascal
FUNCTION SetCompDatTopOfComp(
				object                : HANDLE;
				componentIndex        : INTEGER;
				datumIsTopOfComponent : BOOLEAN): BOOLEAN;
```

```python
def vs.SetCompDatTopOfComp(object, componentIndex, datumIsTopOfComponent):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a slab, roof face, roof, Slab Style, Roof Style, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|datumIsTopOfComponent|BOOLEAN|Whether or not the datum is the top of the component.|

## See Also
VS Functions:
[GetCompDatTopOfComp](GetCompDatTopOfComp.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
