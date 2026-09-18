# CreateCenteredStaticText

## Description
Similar to CreateStaticText, but creates static text that is centered in its control field on the dialog.

```pascal
PROCEDURE CreateCenteredStaticText(
				dialogID          : LONGINT;
				controlID         : LONGINT;
				text              : STRING;
				widthInCharacters : INTEGER);
```

```python
def vs.CreateCenteredStaticText(dialogID, controlID, text, widthInCharacters):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|controlID|LONGINT|   |
|text|STRING|   |
|widthInCharacters|INTEGER|   |

## Examples
```pascal
CreateCenteredStaticText(1, 2, 'Example', 3);
```
```python
import vs

# Similar to CreateStaticText, but creates static text that is centered in
# its control field on the dialog.
dialogID = 1
controlID = 2
text = 'Example text'
widthInCharacters = 3

vs.CreateCenteredStaticText(dialogID, controlID, text, widthInCharacters)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks12.0.1

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
