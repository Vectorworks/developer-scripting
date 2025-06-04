# GetCompDatTopOfComp

## Description
Gets the datum is top of component flag of a component in an object.

```pascal
FUNCTION GetCompDatTopOfComp(
				object                    : HANDLE;
				componentIndex            : INTEGER;
				VAR datumIsTopOfComponent : BOOLEAN): BOOLEAN;
```

```python
def vs.GetCompDatTopOfComp(object, componentIndex):
    return (BOOLEAN, datumIsTopOfComponent)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a slab, roof face, roof, Slab Style, Roof Style, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|datumIsTopOfComponent|BOOLEAN|Returns whether or not the datum is the top of the component.|

## See Also
VS Functions:
[SetCompDatTopOfComp](SetCompDatTopOfComp.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
