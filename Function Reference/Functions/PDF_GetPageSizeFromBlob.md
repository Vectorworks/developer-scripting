# PDF_GetPageSizeFromBlob

## Description
Takes Blob Data and returns corresponding page rect

```pascal
FUNCTION PDF_GetPageSizeFromBlob(
				inBlobPtr    : PROCEDURE;
				inBlobSize   : LONGINT;
				inPageBoxID  : LONGINT;
				inCurPage    : PROCEDURE;
				outBoxLeft   : PROCEDURE;
				outBoxTop    : PROCEDURE;
				outBoxRight  : PROCEDURE;
				outBoxBottom : PROCEDURE): BOOLEAN;
```

```python
def vs.PDF_GetPageSizeFromBlob(inBlobPtr, inBlobSize, inPageBoxID, inCurPage, outBoxLeft, outBoxTop, outBoxRight,  outBoxBottom):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inBlobPtr|PROCEDURE|   |
|inBlobSize|LONGINT|   |
|inPageBoxID|LONGINT|   |
|inCurPage|PROCEDURE|   |
|outBoxLeft|PROCEDURE|   |
|outBoxTop|PROCEDURE|   |
|outBoxRight|PROCEDURE|   |
|outBoxBottom|PROCEDURE|   |

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
