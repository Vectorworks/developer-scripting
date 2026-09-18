# PDF_SetProgressBar

## Description
Sets the progress bar from the PDF Import Menu Command

```pascal
FUNCTION PDF_SetProgressBar(
				progressPtr : PROCEDURE;
				status      : BOOLEAN): BOOLEAN;
```

```python
def vs.PDF_SetProgressBar(progressPtr, status):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|progressPtr|PROCEDURE|   |
|status|BOOLEAN|   |

## Examples
```pascal
resultOK := PDF_SetProgressBar(progressPtr, TRUE);
```
```python
import vs

# Sets the progress bar from the PDF Import Menu Command.
progressPtr = 'Example'
status = True

ok = vs.PDF_SetProgressBar(progressPtr, status)
if ok:
    vs.Message('PDF_SetProgressBar succeeded')
else:
    vs.Message('PDF_SetProgressBar failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
