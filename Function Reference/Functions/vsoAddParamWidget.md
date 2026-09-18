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
|locName|STRING|Localized text that will appear next to the widget. _Note!_ If you specify an empty string, the alternate name of the parameter will be used.|

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

```pascal
bsb := vsoAddParamWidget(1, 'Offset', '');
bsb := vsoAddParamWidget(2, 'Type', '');
bsb := vsoAddParamWidget(3, '__Average Thickness', thicknessLocalized);
bsb := vsoAddParamWidget(4, 'Pitch', '');
bsb := vsoAddParamWidget(5, 'Corrugation Depth', '');

status	:= vsoAddParamWidget( kWidget_RoadLength,		'Road Length', '' );
status	:= vsoAddParamWidget( kWidget_PavingWidth,		'Paving Width', '' );
status	:= vsoAddParamWidget( kWidget_PavingHeight,		'Paving Height', '' );
status	:= vsoAddParamWidget( kWidget_CurbWidth,		'Curb Width', Road_GetLocStr( 'VSRoadwayStraight:param_CurbWidth', '' ) );
status	:= vsoAddParamWidget( kWidget_CurbHeight,		'Curb Height', Road_GetLocStr( 'VSRoadwayStraight:param_CurbHeight', '' ) );
```
```python
def InitParameters():
	# add the widgets
	vs.vsoAddParamWidget( kWidgetID_MarkerSize, 	'Marker Size', '' )
	vs.vsoAppendWidget	( vs.kWidgetButton, 		kWidgetID_StyleButton, vs.GetPluginString( 3002 ), 0 )
	vs.vsoAppendWidget	( vs.kWidgetSeparator, 		kWidgetID_DrawingNumber, vs.GetPluginString( 3003 ), 0 )

def InitParameters():
	# add the widgets the way we like
	vs.vsoAddParamWidget( kWidgetID_Radius, 			'Radius', '' )
	vs.vsoAddParamWidget( kWidgetID_Width, 				'Width', '' )
	vs.vsoAddParamWidget( kWidgetID_CurbHeight,			'Curb Height', vs.Road_GetLocStr( 'VSRoadwayCurved:param_CurbHeight', '' ) )
	vs.vsoAddParamWidget( kWidgetID_CurbWidth,			'Curb Width', vs.Road_GetLocStr( 'VSRoadwayCurved:param_CurbWidth', '' ) )
	vs.vsoAddParamWidget( kWidgetID_PavingThick,		'Paving Thickness', '' )

def InitParameters():
	# add the widgets the way we like
	vs.vsoAddParamWidget( kWidgetID_Width, 				'Road Width', '' )
	vs.vsoAddParamWidget( kWidgetID_CurbHeight,			'Curb Height', vs.Road_GetLocStr( 'VSRoadwayStraight:param_CurbHeight', '' ) )
	vs.vsoAddParamWidget( kWidgetID_CurbWidth,			'Curb Width', vs.Road_GetLocStr( 'VSRoadwayStraight:param_CurbWidth', '' ) )
	vs.vsoAddParamWidget( kWidgetID_PavingThick,		'Paving Thickness', '' )
	vs.vsoAddParamWidget( kWidgetID_Rise, 				'Rise', '' )
```

## Version
Availability: from Vectorworks 2011

## Category
* [Object Events](../Categories/Object%20Events.md)
