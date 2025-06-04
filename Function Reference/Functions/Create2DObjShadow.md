# Create2DObjShadow

## Description
Create a shadow representation of the given 2D object at the specified offset vector.

```pascal
FUNCTION Create2DObjShadow(
				h         : HANDLE;
				offsetVec : REAL): HANDLE;
```

```python
def vs.Create2DObjShadow(h, offsetVec):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to a 2D object.|
|offsetVec|REAL|Shadow direction and length.|

## Examples
==== Python ====
```python
h = vs.FSActLayer()

x = 1
y = 0.5

h_shadow = vs.Create2DObjShadow(h, (x, y))    

# The shadow is not placed on the layer of h.
# This can be fixed with set parent.
vs.SetParent(h_shadow, h.parent)

vs.SetFillBack(h_shadow, (0,0,65000))
vs.SetOpacity(h_shadow, 30)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
