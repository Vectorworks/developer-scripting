# GetOpacity

## Description
Gets the opacity of and object. Opacity is obtained as percentage value in range [0-100].

```pascal
PROCEDURE GetOpacity(
				h           : HANDLE;
				VAR opacity : INTEGER);
```

```python
def vs.GetOpacity(h):
    return opacity
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|The object which opacity will be get.|
|opacity|INTEGER|Output parameter. Return the object's opacity as percentage value in range [0-100].|

## Remarks
If you set opacity to an object inside parametric the actual opacity will be combined with the opacity of the parametric object itself. For example a rectangle with 50% opacity inside a parametric with 50% opacity will actually be rendered with 25% opacity. This behavior is the same for symbols too.

## See Also
[GetOpacity](GetOpacity.md) | [SetOpacity](SetOpacity.md) | [GetOpacityByClass](GetOpacityByClass.md) | [SetOpacityByClass](SetOpacityByClass.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
