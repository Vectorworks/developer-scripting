# CreateColorPopup

## Description
Create a color popup dialog control that displays the 256 color palette associated with the active document.  

The widthInCharacters argument specifies the width of the control.  Pass -1 to request the default size, which will be consistent with other attribute controls (currently defaults to 14).  This argument allows for special circumstances like a small popup for the Fore and Back color associated with the Pattern attribute control.

```pascal
PROCEDURE CreateColorPopup(
				dialogID          : LONGINT;
				itemID            : LONGINT;
				widthInCharacters : LONGINT);
```

```python
def vs.CreateColorPopup(dialogID, itemID, widthInCharacters):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |
|widthInCharacters|LONGINT|   |

## Examples
lorPopupDialog}}

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
