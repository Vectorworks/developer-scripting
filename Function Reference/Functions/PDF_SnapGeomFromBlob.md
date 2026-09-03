# PDF_SnapGeomFromBlob

## Description
Collects vector graphic into ioSnapGeom from the PDF Blob

```pascal
FUNCTION PDF_SnapGeomFromBlob(
				inBlobPtr  : PROCEDURE;
				inBlobSize : LONGINT;
				inCurPage  : LONGINT;
				boundsX    : REAL;
				boundsY    : REAL;
				ioSnapGeom : HANDLE): BOOLEAN;
```

```python
def vs.PDF_SnapGeomFromBlob(inBlobPtr, inBlobSize, inCurPage, boundsX, boundsY, ioSnapGeom):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inBlobPtr|PROCEDURE|   |
|inBlobSize|LONGINT|   |
|inCurPage|LONGINT|   |
|boundsX|REAL|   |
|boundsY|REAL|   |
|ioSnapGeom|HANDLE|   |

## Examples
```pascal
resultOK := PDF_SnapGeomFromBlob(inBlobPtr, 1, 2, 1.0, 2.0, ioSnapGeom);
```
```python
import vs

# Collects vector graphic into ioSnapGeom from the PDF Blob.
inBlobPtr = 'Example'
inBlobSize = 1
inCurPage = 2
boundsX = 1.0
boundsY = 2.0
ioSnapGeom = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.PDF_SnapGeomFromBlob(inBlobPtr, inBlobSize, inCurPage, boundsX, boundsY, ioSnapGeom)
if ok:
    vs.Message('PDF_SnapGeomFromBlob succeeded')
else:
    vs.Message('PDF_SnapGeomFromBlob failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
