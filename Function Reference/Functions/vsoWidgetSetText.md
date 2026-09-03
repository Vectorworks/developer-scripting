# vsoWidgetSetText

## Description
Set the alternate name of a plugin parameter. For a PIO, this text is displayed on the Object Info Palette.

```pascal
PROCEDURE vsoWidgetSetText(
				widgetID : LONGINT;
				text     : STRING);
```

```python
def vs.vsoWidgetSetText(widgetID, text):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |
|text|STRING|   |

## Examples
```pascal
BEGIN
vsoWidgetSetVisible(kCreateButton, TRUE);
IF (tempStr <> '') & (GetObject(tempStr) <> NIL) THEN
	vsoWidgetSetText(kCreateButton, GetPluginString(5007))
ELSE
	vsoWidgetSetText(kCreateButton, GetPluginString(5006));
END;

BEGIN
	vsoWidgetSetText(widgID, Concat(localParam, ' X'));
	vsoWidgetSetText(widgID+1, Concat(localParam, ' Y'));
END;
```
```python
import vs

# Set the alternate name of a plugin parameter.
widgetID = 1
text = 'Example text'

vs.vsoWidgetSetText(widgetID, text)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
