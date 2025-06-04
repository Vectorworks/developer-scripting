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

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
