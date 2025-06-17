# vsoAppendWidget

## Description
Adds a parameter to the Object info palette.

WidgetTypes:
```pascal
	kFieldLongInt     = 1;
	kFieldBoolean     = 2;
	kFieldReal        = 3;
	kFieldText        = 4;
	kFieldCalculation = 5;
	kFieldHandle      = 6;
	kFieldCoordDisp   = 7; {dimension}
	kFieldPopUp       = 8;
	kFieldRadio       = 9;
	kFieldCoordLocX   = 10;	
	kFieldCoordLocY   = 11;

	kWidgetButton     = 12;
	kWidgetStaticText = 13;
	kWidgetDisclosure = 14; {not implemented?}
```

See [[VS:Object Events]].

```pascal
FUNCTION vsoAppendWidget(
				widgetType : LONGINT;
				mappingID  : LONGINT;
				text       : STRING;
				data       : LONGINT):BOOLEAN;
```

```python
def vs.vsoAppendWidget(widgetType, mappingID, text, data):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetType|LONGINT|   |
|mappingID|LONGINT|   |
|text|STRING|   |
|data|LONGINT|   |

## Remarks
This call should be used when a widget is to be added that does not have a corresponding parameter in the object's parameter list (i.e., buttons or static text).

mappingID: a unique number which will be supplied to GetEventInfo to identify which button was pressed.

text:  the widget label.
data:  not implemented at this time.

## Examples
#### VectorScript ####
```pascal
kOnInitPropertiesEventID: 
BEGIN
   resultStatus := SetObjPropVS(kObjectHasUIOverrideID, TRUE);
   resultStatus := vsoAppendParamWidget(1, 'Unused number', 0);
   resultStatus := vsoAppendParamWidget(2, 'Static Text Widget', 0);
   resultStatus := vsoAppendParamWidget(3, 'Enter junk here', 0);
   resultStatus := vsoAppendParamWidget(4, 'Previous static text', 0);
   resultStatus := vsoAppendWidget(kWidgetButton, 1,'Update Text', 0);
END;
```
#### Python ####
```python

```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
