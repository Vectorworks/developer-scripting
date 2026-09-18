# InsertTreeControlItem

## Description
Inserts an item into a Layout Manager tree control.

```pascal
FUNCTION InsertTreeControlItem(
				nDialogID    : LONGINT;
				nComponentID : LONGINT;
				strItemLabel : STRING;
				nParentID    : INTEGER;
				nAfterID     : INTEGER): INTEGER;
```

```python
def vs.InsertTreeControlItem(nDialogID, nComponentID, strItemLabel, nParentID, nAfterID):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|strItemLabel|STRING|   |
|nParentID|INTEGER|   |
|nAfterID|INTEGER|   |

## Examples
```pascal
resultN := InsertTreeControlItem(1, 2, 'Example', 3, 10);
```
```python
import vs

# Inserts an item into a Layout Manager tree control.
nDialogID = 1
nComponentID = 2
strItemLabel = 'Example text'
nParentID = 3
nAfterID = 10

resultN = vs.InsertTreeControlItem(nDialogID, nComponentID, strItemLabel, nParentID, nAfterID)
vs.Message('InsertTreeControlItem returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
