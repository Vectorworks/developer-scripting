# PDF_DrawDCFromBlob

## Description
Draws PDF DocID into passed DC

```pascal
FUNCTION PDF_DrawDCFromBlob(
				inBlobPtr    : PROCEDURE;
				inBlobSize   : LONGINT;
				inCurPage    : LONGINT;
				inDC         : PROCEDURE;
				inDrawMatrix : PROCEDURE;
				inInvalRect  : PROCEDURE;
				inCancelCB   : PROCEDURE): BOOLEAN;
```

```python
def vs.PDF_DrawDCFromBlob(inBlobPtr, inBlobSize, inCurPage, inDC, inDrawMatrix, inInvalRect, inCancelCB):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inBlobPtr|PROCEDURE|   |
|inBlobSize|LONGINT|   |
|inCurPage|LONGINT|   |
|inDC|PROCEDURE|   |
|inDrawMatrix|PROCEDURE|   |
|inInvalRect|PROCEDURE|   |
|inCancelCB|PROCEDURE|   |

## Examples
```pascal
resultOK := PDF_DrawDCFromBlob(inBlobPtr, 1, 2, inDC, inDrawMatrix, inInvalRect, inCancelCB);
```
```python
import vs

# Draws PDF DocID into passed DC.
inBlobPtr = 'Example'
inBlobSize = 1
inCurPage = 2
inDC = 'Example'
inDrawMatrix = 'Example'
inInvalRect = 'Example'
inCancelCB = 'Example'

ok = vs.PDF_DrawDCFromBlob(inBlobPtr, inBlobSize, inCurPage, inDC, inDrawMatrix, inInvalRect, inCancelCB)
if ok:
    vs.Message('PDF_DrawDCFromBlob succeeded')
else:
    vs.Message('PDF_DrawDCFromBlob failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
