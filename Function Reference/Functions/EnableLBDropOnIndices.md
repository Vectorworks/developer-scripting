# EnableLBDropOnIndices

## Description
Enables or disables drag and drop to occur within the specified indices.

```pascal
FUNCTION EnableLBDropOnIndices(
				dialogID    : LONGINT;
				componentID : LONGINT;
				iStartIndex : INTEGER;
				iEndIndex   : INTEGER;
				bEnable     : BOOLEAN): BOOLEAN;
```

```python
def vs.EnableLBDropOnIndices(dialogID, componentID, iStartIndex, iEndIndex, bEnable):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|iStartIndex|INTEGER|   |
|iEndIndex|INTEGER|   |
|bEnable|BOOLEAN|   |

## Examples
```pascal
resultOK := EnableLBDropOnIndices(1, 2, 3, 10, TRUE);
```
```python
import vs

# Enables or disables drag and drop to occur within the specified indices.
dialogID = 1
componentID = 2
iStartIndex = 1
iEndIndex = 1
bEnable = True

ok = vs.EnableLBDropOnIndices(dialogID, componentID, iStartIndex, iEndIndex, bEnable)
if ok:
    vs.Message('EnableLBDropOnIndices succeeded')
else:
    vs.Message('EnableLBDropOnIndices failed')
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
