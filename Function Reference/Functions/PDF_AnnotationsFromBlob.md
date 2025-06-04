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

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
