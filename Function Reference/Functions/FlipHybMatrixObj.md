# FlipHybMatrixObj

## Description
inFlipSpecifier = 0 for flipH, inFlipSpecifier = 1 for FlipV

```pascal
PROCEDURE FlipHybMatrixObj(
				ioHybMatObj     : HANDLE;
				inFlipSpecifier : INTEGER);
```

```python
def vs.FlipHybMatrixObj(ioHybMatObj, inFlipSpecifier):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ioHybMatObj|HANDLE|   |
|inFlipSpecifier|INTEGER|   |

## Remarks
([[User:ykostadinov|Yordan]] 2016.14.09): 
From Vectorworks 2017 it flips object with any rotation.

(*\_c\_* 2015.12.09): 

Started from VWPluginLibraryRoutines.h VW12.

Warning: it only works on symbols or plug-ins whose rotation is 0 or -180. Objects on drawing with any other rotation are ignored.

(*\_c\_* 2008.05.11): 

Flips hybrid objects: symbols and plug-ins. If the objects to flip are symbols you must coerce a redraw for the flip to be visible.
 FlipHybMatrixObj(FSActLayer, 0); { FSActLayer is a symbol on drawing }
 RedrawAll;

## Examples
```pascal
GetSymLoc3D(lNewObj,xctr,yctr,zctr);
SET3DRot(lNewObj, -90, 0, 180, xctr,yctr,zctr);
END;
if  (Caller = 'Utility Cabinet') then
		FlipHybMatrixObj(lNewObj, 0);

BEGIN
	FlipHybMatrixObj( parmHand, 0 );
	bsb := GetEntityMatrix( parmHand, offsetX, offsetY, offsetZ, rotXAngle, rotYAngle, rotZangle );
	bsb := SetEntityMatrix( parmHand, offsetX, offsetY, offsetZ, rotXAngle, rotYAngle, rotZangle+180);
END;

BEGIN
	FlipHybMatrixObj( LNewObj, 1 );
	HMove( LNewObj, 0, HHeight(LNewObj) );
END;
```
```python
import vs

# inFlipSpecifier = 0 for flipH, inFlipSpecifier = 1 for FlipV.
ioHybMatObj = vs.FSActLayer()  # handle to the first selected object on the active layer
inFlipSpecifier = 1

vs.FlipHybMatrixObj(ioHybMatObj, inFlipSpecifier)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
