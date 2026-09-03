# SetPolyClosed

## Description
Sets the open/closed condition of the referenced poly.

```pascal
PROCEDURE SetPolyClosed(
				polyHandle : HANDLE;
				isClosed   : BOOLEAN);
```

```python
def vs.SetPolyClosed(polyHandle, isClosed):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|polyHandle|HANDLE|   |
|isClosed|BOOLEAN|   |

## Examples
```pascal
AddPoint(KickHeight,Y-CabDepth+FaceThick);
AddPoint(KickHeight,Y-CabDepth+KickInset+CabThick);
AddPoint(X,Y-CabDepth+KickInset+CabThick);
EndPoly;
SetPolyClosed(lNewObj,TRUE);
EndXtrd;
SET3DRot(LNewObj, 0, -90, 0, X, Y, 0);

	  in the object as otherwise the lines will not be part of the polyline. }
	tempH := MakePolyline( FInGroup( objH ) );
	GetSegPt2( NextObj( tempH ), tempPt.x, tempPt.y );
	InsertVertex( tempH, tempPt.x, tempPt.y, 4, 0 , 0 );
	SetPolyClosed( tempH, TRUE );
	MakePoly := tempH;
END;

	InsertVertex( polylineH, pX, pY, 1, vertexType, arcRadius );
	SetVertexVisibility( polylineH, 1, TRUE );
END;
DelObject( tempPolyH );
SetPolyClosed(polylineH, TRUE);
```
```python
import vs

# Sets the open/closed condition of the referenced poly.
polyHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
isClosed = False

vs.SetPolyClosed(polyHandle, isClosed)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
