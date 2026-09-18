# SetVertexVisibility

## Description
Sets the visibility of the specified vertex of the referenced object.

```pascal
PROCEDURE SetVertexVisibility(
				h       : HANDLE;
				vertnum : INTEGER;
				vis     : BOOLEAN);
```

```python
def vs.SetVertexVisibility(h, vertnum, vis):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the polygon or polyline.|
|vertnum|INTEGER|Index of the vertex (zero-based).|
|vis|BOOLEAN|Visibility of the vertex.|

## Examples
```pascal
  LineTo(0.049068611093032",-0.020137565169201");
  Add2DVertex(0.044328302938945",-0.001213194214057",4,0.05");
  LineTo(-0.000871161717227",0.027409051114428");
EndPoly;
SetVertexVisibility(LNewObj,6,FALSE);
SetFPat(LNewObj,0);
SetLSN(LNewObj,2);
SetPenFore(LNewObj,6);
SetLW(LNewObj, 15);

FOR vertexNum := 1 TO GetVertNum( tempPolyH ) DO BEGIN
	GetPolylineVertex( tempPolyH, vertexNum, pX, pY, vertexType, arcRadius );
	InsertVertex( polylineH, pX, pY, 1, vertexType, arcRadius );
	SetVertexVisibility( polylineH, 1, TRUE );
END;

{Just closing the poly does not close the open end
	have TO set all vertexes TO visable}
MaxVertIndex := GetVertNum(objH1) - 1;
FOR I := 0 TO MaxVertIndex DO
	SetVertexVisibility (objH1, I, TRUE);
```
```python
import vs

# Sets the visibility of the specified vertex of the referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
vertnum = 1
vis = True

vs.SetVertexVisibility(h, vertnum, vis)
```

## See Also
VS Functions:
[GetVertexVisibility](GetVertexVisibility.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
