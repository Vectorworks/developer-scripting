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

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
