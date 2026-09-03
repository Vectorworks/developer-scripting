# vsoAddWidget

## Description
Add a widget of the specified type and localized name to appear in the Object Info Palette.

```pascal
FUNCTION vsoAddWidget(
				widgetID   : LONGINT;
				widgetType : LONGINT;
				locName    : STRING): BOOLEAN;
```

```python
def vs.vsoAddWidget(widgetID, widgetType, locName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |
|widgetType|LONGINT|   |
|locName|STRING|   |

## Examples
```pascal
boo := vsoAddWidget(Separator_1_ID, kWidgetSeperatorText, koipSeparatorStr);

boo := vsoAddWidget(Separator_1_ID, kWidgetSeperatorText, koipSeparatorStr);
	vsoAppendParameter(PIOName,'AntiAlias');
	vsoAppendParameter(PIOName,'Opacity');
	vsoAppendParameter(PIOName,'FillAtrAsShadowColor');
```
```python
import vs

# Add a widget of the specified type and localized name to appear in the
# Object Info Palette.
widgetID = 1
widgetType = 0
locName = 'Example'

ok = vs.vsoAddWidget(widgetID, widgetType, locName)
if ok:
    vs.Message('vsoAddWidget succeeded')
else:
    vs.Message('vsoAddWidget failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Object Events](../Categories/Object%20Events.md)
