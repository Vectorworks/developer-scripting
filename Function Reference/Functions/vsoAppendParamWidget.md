# vsoAppendParamWidget

## Description
Appends a widget into the OI palette.

See the <a href=http://www.vectorlab.info/index.php?title=Events>VectorLab article</a> on object events.

```pascal
FUNCTION vsoAppendParamWidget(
				parameterID : LONGINT;
				text        : STRING;
				data        : LONGINT):BOOLEAN;
```

```python
def vs.vsoAppendParamWidget(parameterID, text, data):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|parameterID|LONGINT|   |
|text|STRING|   |
|data|LONGINT|   |

## Remarks
This function adds a parameter widget to the end of OIP.

The parameterID corresponds to the ordinal value of the parameter in the object's parameter list.

The text parameter is the label of the parameter to be displayed on the OIP.

The data parameter is currently not in use.

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
   resultStatus := vsoAppendWidget(kWidgetButton, 1, 'Update Text', 0);
END;

**NOTE: For localizations purposes this call should be used in combination 
with the GetLocalizedPluginParameter function as shown below.

If GetLocalizedPluginParameter('NewModelWindowMain','TopShape',temp_s) then
Begin
   result := vsoAppendParamWidget(1,temp_s,eventData);
end;
```
#### Python ####
```python

```

```pascal
IF GetLocalizedPluginParameter('Data Stamp','Date',wString) THEN
	status := vsoAppendParamWidget( 1, wString, 0 );
IF GetLocalizedPluginParameter('Data Stamp','Time',wString) THEN
	status := vsoAppendParamWidget( 2, wString, 0 );
IF GetLocalizedPluginParameter('Data Stamp','FNam',wString) THEN
	status := vsoAppendParamWidget( 3, wString, 0 );

IF GetLocalizedPluginParameter('Drawing Label','Title',wString) THEN
	bsb := vsoAppendParamWidget( 1, wString, 0 );
IF GetLocalizedPluginParameter('Drawing Label','Title Alignment',wString) THEN
	bsb := vsoAppendParamWidget( 2, wString, 0 );
IF GetLocalizedPluginParameter('Drawing Label','Drawing',wString) THEN
	bsb := vsoAppendParamWidget( 3, wString, 0 );

BEGIN
	If GetLocalizedPluginParameter(recName, fldName, locFldName) then BEGIN
		result := vsoAppendParamWidget(GetFldIndex(GetObject(recName), fldName), locFldName, 0);
	END;
```
```python
result = vs.vsoAppendParamWidget(parameterID, 'Example', data)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
