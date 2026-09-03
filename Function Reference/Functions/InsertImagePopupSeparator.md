# InsertImagePopupSeparator

## Description
Inserts a separator with the specified label at the end of the image popup list.

```pascal
FUNCTION InsertImagePopupSeparator(
				liDialogID    : LONGINT;
				liComponentID : LONGINT;
				strLabel      : STRING): INTEGER;
```

```python
def vs.InsertImagePopupSeparator(liDialogID, liComponentID, strLabel):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|liDialogID|LONGINT|   |
|liComponentID|LONGINT|   |
|strLabel|STRING|   |

## Examples
```pascal
resultN := InsertImagePopupSeparator(1, 2, 'Example');
```
```python
import vs

# Inserts a separator with the specified label at the end of the image popup
# list.
liDialogID = 1
liComponentID = 2
strLabel = 'Example text'

resultN = vs.InsertImagePopupSeparator(liDialogID, liComponentID, strLabel)
vs.Message('InsertImagePopupSeparator returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
