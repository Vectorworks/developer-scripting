# PDF_GetPageMatrixFromBlob

## Description
Get PDF Default Matrix.

```pascal
FUNCTION PDF_GetPageMatrixFromBlob(
				inBlobPtr  : PROCEDURE;
				inBlobSize : LONGINT;
				inCurPage  : LONGINT;
				inMatrix   : PROCEDURE): BOOLEAN;
```

```python
def vs.PDF_GetPageMatrixFromBlob(inBlobPtr, inBlobSize, inCurPage, inMatrix):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inBlobPtr|PROCEDURE|   |
|inBlobSize|LONGINT|   |
|inCurPage|LONGINT|   |
|inMatrix|PROCEDURE|   |

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
