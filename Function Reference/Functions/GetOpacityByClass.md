# GetOpacityByClass

## Description
Returns whether the object is using the class opacity.

```pascal
PROCEDURE GetOpacityByClass(
				h             : HANDLE;
				VAR isByClass : BOOLEAN);
```

```python
def vs.GetOpacityByClass(h):
    return isByClass
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|The object which opacity will be get.|
|isByClass|BOOLEAN|Output parameter. Returns TRUE if this object's opacity is determined by its class.|

## Remarks
If you set opacity to an object inside parametric the actual opacity will be combined with the opacity of the parametric object itself. For example a rectangle with 50% opacity inside a parametric with 50% opacity will actually be rendered with 25% opacity. This behavior is the same for symbols too.

## See Also
[GetOpacity](GetOpacity.md) | [SetOpacity](SetOpacity.md) | [GetOpacityByClass](GetOpacityByClass.md) | [SetOpacityByClass](SetOpacityByClass.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
