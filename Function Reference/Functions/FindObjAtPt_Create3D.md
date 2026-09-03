# FindObjAtPt_Create3D

## Description
Creates object find for objects at specified point within specified radius. The function is capable of iterating

```pascal
FUNCTION FindObjAtPt_Create3D(
				hContainer  : HANDLE;
				objOptions  : INTEGER;
				travOptions : INTEGER;
				locX        : REAL;
				locY        : REAL;
				locZ        : REAL;
				pickRadius  : REAL): LONGINT;
```

```python
def vs.FindObjAtPt_Create3D(hContainer, objOptions, travOptions, locX, locY, locZ, pickRadius):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hContainer|HANDLE|   |
|objOptions|INTEGER|   |
|travOptions|INTEGER|   |
|locX|REAL|   |
|locY|REAL|   |
|locZ|REAL|   |
|pickRadius|REAL|   |

## Examples
```pascal
resultN := FindObjAtPt_Create3D(hContainer, 1, 2, 1.0, 2.0, 0.5, 1.5);
```
```python
import vs

# Creates object find for objects at specified point within specified radius.
hContainer = vs.FSActLayer()  # handle to the first selected object on the active layer
objOptions = 1
travOptions = 2
locX = 1.0
locY = 2.0
locZ = 0.5
pickRadius = 1.0

resultN = vs.FindObjAtPt_Create3D(hContainer, objOptions, travOptions, locX, locY, locZ, pickRadius)
vs.Message('FindObjAtPt_Create3D returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2020

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
