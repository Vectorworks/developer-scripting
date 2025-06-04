# SubtractSolid

## Description
Function SubtractSolid creates a new solid subtraction object from the referenced source objects.

{| class="wikitable_c"
|+ Table - Solids Operation Result Codes
! Operation Result !! Result Code
|-
| Success
| 0
|-
| Null geometry error
| 1
|-
| Geometry error
| 2
|-
| Out of memory error
| 4
|-
| Bad group error
| 5
|-
| Invalid object type
| 6
|-
| Bad input
| 20
|}

```pascal
FUNCTION SubtractSolid(
				obj1         : HANDLE;
				obj2         : HANDLE;
				VAR newSolid : HANDLE): INTEGER;
```

```python
def vs.SubtractSolid(obj1, obj2):
    return (INTEGER, newSolid)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj1|HANDLE|Handle to source object for subtract operation.|
|obj2|HANDLE|Handle to source object for subtract operation.|
|newSolid|HANDLE|Handle to resultant object from subtract operation.|

## Remarks
[[User:CBM-c-|_c_]] (2018.02.11):  obj1 = clipped, obj2 = clipper

Everything cuts the backmost object, which will be the 1st retrived using [[VS:FIn3D]].

A solid subtraction has object type 84 and subtype 516. Mind, also other objects have type 84, such as Generic Solids (eventually generated using [[VS:ExtrudeAlongPath]])

## Version
Availability: from MiniCAD 7.0

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
