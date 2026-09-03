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

## Examples
```pascal
cLocPathLengthInMM	:= OLDSetHangPathHandle( ghParm, 0, hPath, AllZ, FALSE );

cLocPathLengthInMM	:= OLDSetHangPathHandle( ghParm, 0, hPath, cArrayHeight, FALSE );

cLocPathLengthInMM	:= OLDSetHangPathHandle( ghParm, kLoadScreenIndex, hPath, AllZ, FALSE );
```
```python
import vs

# Adds the path to the hang points of the specified load for the parametric
# object.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
loadIndex = 1
path = 'C:/Temp'
height = 2.0
deletePathHandle = True

vs.OLDSetHangPathHandle(handle, loadIndex, path, height, deletePathHandle)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
