# vsoWidgetPopupEnergy

## Description
Attach a widget for energy data to appear in the Object Info Palette.

```pascal
PROCEDURE vsoWidgetPopupEnergy(
				widgetID : LONGINT;
				dataType : INTEGER);
```

```python
def vs.vsoWidgetPopupEnergy(widgetID, dataType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |
|dataType|INTEGER|   |

## Examples
```pascal
vsoWidgetPopupEnergy(1, 2);
```
```python
import vs

# Attach a widget for energy data to appear in the Object Info Palette.
widgetID = 1
dataType = 0

vs.vsoWidgetPopupEnergy(widgetID, dataType)
```

## Version
Availability: from Vectorworks 2016

## Category
* [Object Events](../Categories/Object%20Events.md)
