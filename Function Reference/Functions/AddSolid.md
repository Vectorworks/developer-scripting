# AddSolid

## Description
Function AddSolid creates a new solid addition object from the referenced source objects. If the operation succeeds, the source objects will then be contained within the newSolid object, as the primitives which define the CSG.

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
|-
| Handles not in document
| 21
|}

```pascal
FUNCTION AddSolid(
				obj1         : HANDLE;
				obj2         : HANDLE;
				VAR newSolid : HANDLE): INTEGER;
```

```python
def vs.AddSolid(obj1, obj2):
    return (INTEGER, newSolid)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj1|HANDLE|Handle to source object for add operation.|
|obj2|HANDLE|Handle to source object for add operation.|
|newSolid|HANDLE|Handle to resultant object from add operation.|

## Examples
ginXtrd}}

## Version
Availability: from MiniCAD 7.0

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
