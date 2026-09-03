# PDF_AnnotationsFromBlob

## Description
Draws annotations from the PDF Blob

```pascal
FUNCTION PDF_AnnotationsFromBlob(
				inBlobPtr  : PROCEDURE;
				inBlobSize : LONGINT;
				inCurPage  : LONGINT;
				boundsX    : REAL;
				boundsY    : REAL;
				ioSnapGeom : HANDLE): BOOLEAN;
```

```python
def vs.PDF_AnnotationsFromBlob(inBlobPtr, inBlobSize, inCurPage, boundsX, boundsY, ioSnapGeom):
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
resultOK := PDF_AnnotationsFromBlob(inBlobPtr, 1, 2, 1.0, 2.0, ioSnapGeom);
```
```python
import vs

# Draws annotations from the PDF Blob.
inBlobPtr = 'Example'
inBlobSize = 1
inCurPage = 2
boundsX = 1.0
boundsY = 2.0
ioSnapGeom = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.PDF_AnnotationsFromBlob(inBlobPtr, inBlobSize, inCurPage, boundsX, boundsY, ioSnapGeom)
if ok:
    vs.Message('PDF_AnnotationsFromBlob succeeded')
else:
    vs.Message('PDF_AnnotationsFromBlob failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
