# PDF_CreatePDFABlobFromBlob

## Description
Takes Blob Data and creates a PDFA blob

```pascal
FUNCTION PDF_CreatePDFABlobFromBlob(
				inBlobPtr    : PROCEDURE;
				inBlobSize   : LONGINT;
				inPDFAFormat : LONGINT;
				ioBlobPtr    : PROCEDURE;
				ioBlobSize   : PROCEDURE): BOOLEAN;
```

```python
def vs.PDF_CreatePDFABlobFromBlob(inBlobPtr, inBlobSize, inPDFAFormat, ioBlobPtr, ioBlobSize):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inBlobPtr|PROCEDURE|   |
|inBlobSize|LONGINT|   |
|inPDFAFormat|LONGINT|   |
|ioBlobPtr|PROCEDURE|   |
|ioBlobSize|PROCEDURE|   |

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
