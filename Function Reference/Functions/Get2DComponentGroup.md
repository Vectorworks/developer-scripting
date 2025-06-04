# Get2DComponentGroup

## Description
Gets the specified 2D component group of a symbol definition or plug-in object or NULL if the group does not exist.


''Table - 2D components''
{| class = "wikitable_c"
! Constant !! 2D component
|-
| 0 || Not Set
|-
| 1 || Top
|-
| 2 || Bottom
|-
| 3 || Top and Bottom Cut
|-
| 4 || Front
|-
| 5 || Back
|-
| 6 || Front and Back Cut
|-
| 7 || Left
|-
| 8 || Right
|-
| 9  || Left and Right Cut 
|}

```pascal
FUNCTION Get2DComponentGroup(
				objectHandle : HANDLE;
				component    : INTEGER): HANDLE;
```

```python
def vs.Get2DComponentGroup(objectHandle, component):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to the object.|
|component|INTEGER|2D component.|

## See Also
VS Functions:
[Set2DComponentGroup](Set2DComponentGroup.md) 
| [SetTopPlan2DComp](SetTopPlan2DComp.md) 
| [GetTopPlan2DComp](GetTopPlan2DComp.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
