# PDF_CreateBlob

## Description
Creates a memory blob representation of a specified document and page.

```pascal
FUNCTION PDF_CreateBlob(
				inFilePath : PROCEDURE;
				ioBlobPtr  : PROCEDURE;
				ioBlobSize : PROCEDURE;
				ioCurPage  : PROCEDURE): BOOLEAN;
```

```python
def vs.PDF_CreateBlob(inFilePath, ioBlobPtr, ioBlobSize, ioCurPage):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inFilePath|PROCEDURE|   |
|ioBlobPtr|PROCEDURE|   |
|ioBlobSize|PROCEDURE|   |
|ioCurPage|PROCEDURE|   |

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
