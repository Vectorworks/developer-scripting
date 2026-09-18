# OLDAddLoadHangPoint

## Description
Adds hang point of the speciafied load for the parametric object

```pascal
PROCEDURE OLDAddLoadHangPoint(
				handle    : HANDLE;
				loadIndex : INTEGER;
				point     : VECTOR;
				hasLoad   : BOOLEAN);
```

```python
def vs.OLDAddLoadHangPoint(handle, loadIndex, point, hasLoad):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|loadIndex|INTEGER|   |
|point|VECTOR|   |
|hasLoad|BOOLEAN|   |

## Examples
```pascal
OLDAddLoadHangPoint( ghParm, 0, finalPt, TRUE );

	OLDAddLoadHangPoint( ghParm, 0, tmpPt, TRUE );
END;

	Get3DInfo( geometry, height, width, depth );
	resultPt.x	:= pX;
	resultPt.y	:= py;
	resultPt.z	:= pZ + depth/2;
	OLDAddLoadHangPoint( ghParm, Index, resultPt, TRUE );
END;
```
```python
import vs

# Adds hang point of the speciafied load for the parametric object.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
loadIndex = 1
point = (0, 0)
hasLoad = True

vs.OLDAddLoadHangPoint(handle, loadIndex, point, hasLoad)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
