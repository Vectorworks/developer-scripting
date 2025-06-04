# vsoInsertWidget

## Description
This function inserts a widget into the ObjectInfoPalette. It allows the user to define the location of where this widget will be in the OIP widget list.

WidgetTypes:
<code lang="pas">
	kFieldLongInt     	= 1;
	kFieldBoolean     	= 2;
	kFieldReal        	= 3;
	kFieldText       	= 4;
	kFieldCalculation 	= 5;
	kFieldHandle      	= 6;
	kFieldCoordDisp   	= 7; {dimension}
	kFieldPopUp       	= 8;
	kFieldRadio       	= 9;
	kFieldCoordLocX   	= 10;	
	kFieldCoordLocY   	= 11;
	kWidgetButton     	= 12;
	kWidgetStaticText 	= 13;
	kFieldStaticText  	= 14;
        kWidgetDimStdPopUp	= 16;
	kWidgetPrecisionPopUp	= 17;
	kWidgetClassesPopup	= 18;
	kWidgetLayersPopup	= 19;
	kWidgetAngleDisp	= 20;
	kWidgetAreaDisp		= 21;
	kWidgetVolumeDisp	= 22;
	kWidgetSeparator	= 100;
	kWidgetSubSelection	= 101;
	kWidgetBoundPopup	= 102;
	kWidgetBoundOffset	= 103;
</code>

See [[VS:Object Events]].

```pascal
FUNCTION vsoInsertWidget(
				paramID    : LONGINT;
				widgetType : LONGINT;
				mappingID  : LONGINT;
				text       : STRING;
				data       : LONGINT):BOOLEAN;
```

```python
def vs.vsoInsertWidget(paramID, widgetType, mappingID, text, data):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|paramID|LONGINT|The ID and location of where this widget will be displayed in the OIP.|
|widgetType|LONGINT|Type of widget to create.|
|mappingID|LONGINT|Ordinal value of object parameter that corresponds to this widget.|
|text|STRING|The label to be displayed on OIP for this widget.|
|data|LONGINT|Not implemented yet.|

## Remarks
At least in 2008, there might be a bug in this call. The "mappingID" argument doesn't seem to be registering the index of the widget properly, and as a result, if the widget is a button, you won't get the proper index in the button click event. 
If somebody fully investigates this, and determines that it's a bug, he/she should enter a bug report.

vsoAppendWidget still works OK.

It looks like the problem occurs if you don't declare kObjXPropHasUIOverride (kObjXPropHasUIOverride is FALSE or not declared):

<code lang="pas">
result := SetObjPropVS(kObjXPropHasUIOverride, TRUE);
</code>

## Examples
#### VectorScript ####
```pascal
kOnInitPropertiesEventID: 
BEGIN
   resultStatus := SetObjPropVS(kObjectHasUIOverrideID, TRUE);
   resultStatus := vsoInsertParamWidget(1,1, 'Unused number', 0);
   resultStatus := vsoInsertParamWidget(2,2, 'Static Text Widget', 0);
   resultStatus := vsoInsertParamWidget(3,3, 'Enter junk here', 0);
   resultStatus := vsoInsertParamWidget(4,4, 'Previous static text', 0);
   resultStatus := vsoInsertWidget(5,kWidgetButton, 5,'Update Text', 0);
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
