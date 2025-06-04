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

## Version
Availability: from Vectorworks 2020

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
