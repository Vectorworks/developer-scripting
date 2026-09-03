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

## Examples
```pascal
BEGIN
	NumCav := GetObjectVariableInt(h,199);
	For I := 1 to NumCav DO
		BSB := DeleteComponent(h,1);
END;
```
```python
import vs

# Deletes a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok = vs.DeleteComponent(obj, componentIndex)
if ok:
    vs.Message('DeleteComponent succeeded')
else:
    vs.Message('DeleteComponent failed')
```

## See Also
VS Functions:
[InsertNewComponent](InsertNewComponent.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
