# GetComponentRect

## Description
Retrieves the bounding rect coordinates of the specified Layout Manager component.

```pascal
FUNCTION GetComponentRect(
				nDialogID    : LONGINT;
				nComponentID : LONGINT;
				VAR nLeft    : INTEGER;
				VAR nTop     : INTEGER;
				VAR nRight   : INTEGER;
				VAR nBottom  : INTEGER): BOOLEAN;
```

```python
def vs.GetComponentRect(nDialogID, nComponentID):
    return (BOOLEAN, nLeft, nTop, nRight, nBottom)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nLeft|INTEGER|   |
|nTop|INTEGER|   |
|nRight|INTEGER|   |
|nBottom|INTEGER|   |

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
