# OLDSetHangPathHandle

## Description
Adds the path to the hang points of the specified load for the parametric object

```pascal
PROCEDURE OLDSetHangPathHandle(
				handle           : HANDLE;
				loadIndex        : INTEGER;
				path             : HANDLE;
				height           : REAL;
				deletePathHandle : BOOLEAN);
```

```python
def vs.OLDSetHangPathHandle(handle, loadIndex, path, height, deletePathHandle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|loadIndex|INTEGER|   |
|path|HANDLE|   |
|height|REAL|   |
|deletePathHandle|BOOLEAN|   |

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
