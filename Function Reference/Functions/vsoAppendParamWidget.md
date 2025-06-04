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

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
