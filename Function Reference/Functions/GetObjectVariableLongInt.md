# GetObjectVariableLongInt

## Description
Returns the value of a VectorWorks object property. Used with properties returning a LONGINT value.

For specific object selector index values, see the [Script Appendix](../Appendix/pages/Appendix%20G%20-%20Object%20Selectors.md).

```pascal
FUNCTION GetObjectVariableLongInt(
				h     : HANDLE;
				index : INTEGER): LONGINT;
```

```python
def vs.GetObjectVariableLongInt(h, index):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|

## Examples
#### VectorScript ####
```pascal
p:= GetObjectVariableLongInt(h,579);
```
#### Python ####
```python
p = vs.GetObjectVariableLongInt(h,579)
```

```pascal
pioPhotoObjHand := CreatePaintFromImgN( pioPhotoRsrcHand, 0, 0, 0 );
pioPhotoRsrcWidth := HWidth( pioPhotoObjHand );
pioPhotoRsrcHeight := HHeight( pioPhotoObjHand );
pioPhotoRsrcPixelW := GetObjectVariableLongint( pioPhotoObjHand, 530 );
pioPhotoRsrcPixelH := GetObjectVariableLongint( pioPhotoObjHand, 531 );
{ instead of keeping a bitmap of the inage, delete it and create a similar size rectangle as a place holder }
DelObjectClearHandProc( pioPhotoObjHand );
RectangleN( -pioPhotoRsrcWidth / 2, -pioPhotoRsrcHeight / 2, 1, 0, pioPhotoRsrcWidth, pioPhotoRsrcHeight );
```
```python
import vs

# Returns the value of a VectorWorks object property.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1

resultN = vs.GetObjectVariableLongInt(h, index)
vs.Message('GetObjectVariableLongInt returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
