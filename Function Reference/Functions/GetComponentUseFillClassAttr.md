# GetComponentUseFillClassAttr

## Description
Gets the use fill class attributes flag of a component in an object.

```pascal
FUNCTION GetComponentUseFillClassAttr(
				obj                        : HANDLE;
				componentIndex             : INTEGER;
				VAR useFillClassAttributes : BOOLEAN): BOOLEAN;
```

```python
def vs.GetComponentUseFillClassAttr(obj, componentIndex):
    return (BOOLEAN, useFillClassAttributes)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useFillClassAttributes|BOOLEAN|Returns whether or not the component is using class attributes for its fill.|

## See Also
VS Functions:
[SetComponentUseFillClassAttr](SetComponentUseFillClassAttr.md)

## Version
Availability: from VectorWorks 2008

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
