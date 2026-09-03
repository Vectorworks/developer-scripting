# CreateThreeStateCheckBox

## Description
Creates a Layout Manager three state checkbox.

```pascal
PROCEDURE CreateThreeStateCheckBox(
				dialogID    : LONGINT;
				componentID : LONGINT;
				strName     : STRING);
```

```python
def vs.CreateThreeStateCheckBox(dialogID, componentID, strName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|strName|STRING|   |

## Examples
```pascal
CreateThreeStateCheckBox(1, 2, 'Example');
```
```python
import vs

# Creates a Layout Manager three state checkbox.
dialogID = 1
componentID = 2
strName = 'Example'

vs.CreateThreeStateCheckBox(dialogID, componentID, strName)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
