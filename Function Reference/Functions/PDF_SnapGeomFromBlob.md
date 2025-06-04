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

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
