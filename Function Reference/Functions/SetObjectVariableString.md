# SetObjectVariableString

## Description
Sets the value of a VectorWorks object property. Used with properties requiring a STRING value.

For specific object selector index values, see the [Script Appendix](../Appendix/pages/Appendix%20G%20-%20Object%20Selectors.md).

```pascal
PROCEDURE SetObjectVariableString(
				h     : HANDLE;
				index : INTEGER;
				value : STRING);
```

```python
def vs.SetObjectVariableString(h, index, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|
|value|STRING|New value for property.|

## Examples
#### VectorScript ####
```pascal
SetPref(17,FALSE);
```
#### Python ####
```python

```

```pascal
BEGIN
	vpTitle := GetObjectVariableString(vpHand, 1032);
	IF vpTitle <> pTitle THEN
		SetObjectVariableString(vpHand, 1032, pTitle);
	vpLocator := GetObjectVariableString(vpHand, 1033);
	IF vpLocator <> gDrawing THEN
	BEGIN
		SetObjectVariableString(vpHand, 1033, gDrawing);    { If the Drawing(Item) the user types in is not unique, SetObjectVariableString won't set the viewport locator field.}

END;
if wsHand = nil then BEGIN
	wsHand := CreateWS(wsName, kNumRows, kNumCols);
	SetWSPlacement          (wsHand, 186, 49, 450, 672);
	SetObjectVariableString (wsHand, 80, wsName); {Worksheet Header}
	SetObjectVariableBoolean(wsHand, 82, FALSE);  {Show Database Header}
	SetObjectVariableBoolean(wsHand, 83, FALSE);  {Show Gridlines}
	SetObjectVariableInt    (wsHand, 86, GetFontID('Arial')); {Default Font Index}
	SetObjectVariableInt    (wsHand, 87, 10);     {Default Font Size}

BEGIN
	currFieldValue := GetRField(pluginH, recordName, gFieldName [i]);
	pluginLayer := GetLayer(pluginH);
	IF (currFieldValue <> gFieldValue[i]) & (GetObjectVariableInt(pluginLayer, 154) = 2) THEN { check if drawing border is on a sheet layer}
		SetObjectVariableString(pluginLayer, 159, gFieldValue[i]);
END;
```
```python
vs.SetObjectVariableString(h, 1, value)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
