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

## Examples
```pascal
resultOK := PDF_CreateBlob(inFilePath, ioBlobPtr, ioBlobSize, ioCurPage);
```
```python
import vs

# Creates a memory blob representation of a specified document and page.
inFilePath = 'C:/Temp'
ioBlobPtr = 'Example'
ioBlobSize = 1.0
ioCurPage = 'Example'

ok = vs.PDF_CreateBlob(inFilePath, ioBlobPtr, ioBlobSize, ioCurPage)
if ok:
    vs.Message('PDF_CreateBlob succeeded')
else:
    vs.Message('PDF_CreateBlob failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
