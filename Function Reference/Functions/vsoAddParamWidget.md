# vsoAddParamWidget

## Description
Add a widget for parameter to appear in the Object Info Palette.

```pascal
FUNCTION vsoAddParamWidget(
				widgetID  : LONGINT;
				paramName : STRING;
				locName   : STRING): BOOLEAN;
```

```python
def vs.vsoAddParamWidget(widgetID, paramName, locName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|A unique number specified by the user to identify this widget.|
|paramName|STRING|The universal name of the parameter.|
|locName|STRING|Localized text that will appear next to the widget. <b>Note!</b> If you specify an empty string, the alternate name of the parameter will be used.|

## Examples
```python
# add the widgets the way we like    
    ok = vs.vsoAddParamWidget( kWidgetID_TotalHeight, 'height', '' )
    ok = vs.vsoAddParamWidget( kWidgetID_HeadShape, 'Head Shape', '' )
    ok = vs.vsoAddParamWidget( kWidgetID_Sex, 'Sex', '' )
    ok = vs.vsoAddParamWidget( kWidgetID_Hair, 'Hair', '' )
    ok = vs.vsoAddParamWidget( kWidgetID_HairLen, 'Hair Length', '' )
    vs.vsoWidgetSetIndLvl( kWidgetID_HairLen, 1 )
    ok = vs.vsoAddWidget( kWidgetID_DefaultHairLen, 12, 'Reset Default' )
    vs.vsoWidgetSetIndLvl( kWidgetID_DefaultHairLen, 1 )
```

## Version
Availability: from Vectorworks 2011

## Category
* [Object Events](../Categories/Object%20Events.md)
