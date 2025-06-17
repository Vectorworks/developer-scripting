# DeleteComponent

## Description
Deletes a component in an object.

```pascal
FUNCTION DeleteComponent(
				obj            : HANDLE;
				componentIndex : INTEGER): BOOLEAN;
```

```python
def vs.DeleteComponent(obj, componentIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component to delete.|

## Remarks
*\_c\_*: (2016.02.03):  Supports also Roof and Roof Styles components from VW 2016.

## See Also
VS Functions:
[InsertNewComponent](InsertNewComponent.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
