# SetWSPlacement

## Description
Sets the on-screen location and dimensions of the referenced worksheets' window.

```pascal
PROCEDURE SetWSPlacement(
				worksheet : HANDLE;
				top       : INTEGER;
				left      : INTEGER;
				bottom    : INTEGER;
				right     : INTEGER);
```

```python
def vs.SetWSPlacement(worksheet, top, left, bottom, right):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|top|INTEGER|X-coordinate of top left corner of worksheet window.|
|left|INTEGER|Y-coordinate of top left corner of worksheet window.|
|bottom|INTEGER|X-coordinate of bottom right corner of worksheet window.|
|right|INTEGER|Y-coordinate of bottom right corner of worksheet window.|

## Examples
```pascal
BEGIN
		DefaultWSFontID := GetObjectVariableInt(tempHandle,86);
		SetWSPlacement(tempHandle,130,223,698,816);
		{SetObjectVariableInt(tempHandle,86,0);} {Don't do this!!!!}
		SetObjectVariableInt(tempHandle,87,10);
		{Column Widths}
		SetWSColumnWidth(tempHandle,1,1,80);

	END;
END;
if wsHand = nil then BEGIN
	wsHand := CreateWS(wsName, kNumRows, kNumCols);
	SetWSPlacement          (wsHand, 186, 49, 450, 672);
	SetObjectVariableString (wsHand, 80, wsName); {Worksheet Header}
	SetObjectVariableBoolean(wsHand, 82, FALSE);  {Show Database Header}
	SetObjectVariableBoolean(wsHand, 83, FALSE);  {Show Gridlines}
	SetObjectVariableInt    (wsHand, 86, GetFontID('Arial')); {Default Font Index}

{Creation/Placement}
tempHandle := CreateWS(gWKSName, (targetCnt + 5), 3);
SetWSPlacement(tempHandle,0,0,0,0);
SetObjectVariableInt(tempHandle,87,10);
```
```python
import vs

# Sets the on-screen location and dimensions of the referenced worksheets'
# window.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
top = 1
left = 2
bottom = 3
right = 10

vs.SetWSPlacement(worksheet, top, left, bottom, right)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
