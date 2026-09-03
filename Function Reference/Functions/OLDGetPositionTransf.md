# OLDGetPositionTransf

## Description
Returns TRUE if the position where the load is attached is moved/rotated. Gets the offset applied to the load in object local coordinates and the rotation angle applied to the position. HasWitnessLine point weather the object is already connected via a witness line

```pascal
FUNCTION OLDGetPositionTransf(
				handle             : HANDLE;
				loadIndex          : INTEGER;
				VAR offsetDistance : VECTOR;
				VAR rotationAngle  : REAL;
				VAR hasWitnessLine : BOOLEAN): BOOLEAN;
```

```python
def vs.OLDGetPositionTransf(handle, loadIndex):
    return (BOOLEAN, offsetDistance, rotationAngle, hasWitnessLine)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|loadIndex|INTEGER|   |
|offsetDistance|VECTOR|   |
|rotationAngle|REAL|   |
|hasWitnessLine|BOOLEAN|   |

## Examples
```pascal
BEGIN
	posProjMoved	:= OLDGetPositionTransf( ghParm, kLoadProjector1Index, posOffset, posRot, hasWitnessLine );

BEGIN
	posProjMoved	:= OLDGetPositionTransf( ghParm, kLoadProjector1Index, posOffset, posRot, hasWitnessLine );
	posScrMoved		:= OLDGetPositionTransf( ghParm, kLoadScreenIndex, posOffset, posRot, hasWitnessLine );
```
```python
import vs

# Returns TRUE if the position where the load is attached is moved/rotated.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
loadIndex = 1

ok, offsetDistance, rotationAngle, hasWitnessLine = vs.OLDGetPositionTransf(handle, loadIndex)
vs.Message('OLDGetPositionTransf returned: ' + str((ok, offsetDistance, rotationAngle, hasWitnessLine)))
```

## Version
Availability: from Vectorworks 2019

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
