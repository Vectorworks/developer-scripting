# PDF_GetPageCount

## Description
Returns the page count of the selected document file.

```pascal
FUNCTION PDF_GetPageCount(inFilePath : PROCEDURE): INTEGER;
```

```python
def vs.PDF_GetPageCount(inFilePath):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inFilePath|PROCEDURE|   |

## Examples
```pascal
resultN := PDF_GetPageCount(inFilePath);
```
```python
import vs

# Returns the page count of the selected document file.
inFilePath = 'C:/Temp'

count = vs.PDF_GetPageCount(inFilePath)
vs.Message('PDF_GetPageCount returned: ' + str(count))
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
