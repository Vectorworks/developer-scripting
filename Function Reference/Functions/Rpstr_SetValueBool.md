# Rpstr_SetValueBool

## Description
Set a boolean value from the VectorScript value repository.

```pascal
PROCEDURE Rpstr_SetValueBool(
				name  : STRING;
				value : BOOLEAN);
```

```python
def vs.Rpstr_SetValueBool(name, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|The name of the value.|
|value|BOOLEAN|Set a value associated with the name in the VectorScript value repository.|

## Examples
```pascal
BEGIN
	Rpstr_SetValueBool('IsRegistered',TRUE);
	{This tells VW to let the object decide what goes onto the Object Info palette.}
	result:= SetObjPropVS(kObjXPropHasUIOverride, TRUE);
	result := SetObjPropVS(12, TRUE); {kObjXHasCustomWidgetVisibilities}
	result := SetObjPropVS (kObjXHasCustomWidgetVisibilities,TRUE);	{Is this needed to use "SetParameterVisibility()" }

BEGIN
	Rpstr_SetValueBool('IsRegistered',TRUE);
	{This tells VW to let the object decide what goes onto the Object Info palette.}
	result:= SetObjPropVS(kObjXPropHasUIOverride, TRUE);
	result := SetObjPropVS(12, TRUE); {kObjXHasCustomWidgetVisibilities}

BEGIN
	AlrtDialog('#1 You have been using AutpPlot Tools for longer than 3 months.  Please register.  See the first AutoPlot menu item');
	Rpstr_SetValueBool('IsRegistered',FALSE);
END
```
```python
import vs

# Set a boolean value from the VectorScript value repository.
name = 'Example'
value = True

vs.Rpstr_SetValueBool(name, value)
```

## See Also
VS Functions:
[Rpstr_RemoveValues](Rpstr_RemoveValues.md) 
| [Rpstr_RemoveValue](Rpstr_RemoveValue.md) 
| [Rpstr_GetValueBool](Rpstr_GetValueBool.md) 
| [Rpstr_SetValueBool](Rpstr_SetValueBool.md) 
| [Rpstr_GetValueInt](Rpstr_GetValueInt.md) 
| [Rpstr_SetValueInt](Rpstr_SetValueInt.md) 
| [Rpstr_GetValueReal](Rpstr_GetValueReal.md) 
| [Rpstr_SetValueReal](Rpstr_SetValueReal.md) 
| [Rpstr_GetValueStr](Rpstr_GetValueStr.md) 
| [Rpstr_SetValueStr](Rpstr_SetValueStr.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Utility](../Categories/Utility.md)
