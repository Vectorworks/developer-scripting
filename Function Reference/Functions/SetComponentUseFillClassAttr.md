# SetComponentUseFillClassAttr

## Description
Sets the use fill class attributes flag of a component in an object.

```pascal
FUNCTION SetComponentUseFillClassAttr(
				obj                    : HANDLE;
				componentIndex         : INTEGER;
				useFillClassAttributes : BOOLEAN): BOOLEAN;
```

```python
def vs.SetComponentUseFillClassAttr(obj, componentIndex, useFillClassAttributes):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useFillClassAttributes|BOOLEAN|Whether or not the component will use class attributes for its fill.|

## See Also
VS Functions:
[GetComponentUseFillClassAttr](GetComponentUseFillClassAttr.md)

## Version
Availability: from VectorWorks 2008

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
