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

## Examples
```pascal
resultOK := PDF_GetPageMatrixFromBlob(inBlobPtr, 1, 2, inMatrix);
```
```python
import vs

# Get PDF Default Matrix.
inBlobPtr = 'Example'
inBlobSize = 1
inCurPage = 2
inMatrix = 'Example'

ok = vs.PDF_GetPageMatrixFromBlob(inBlobPtr, inBlobSize, inCurPage, inMatrix)
if ok:
    vs.Message('PDF_GetPageMatrixFromBlob succeeded')
else:
    vs.Message('PDF_GetPageMatrixFromBlob failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
