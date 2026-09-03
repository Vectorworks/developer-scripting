# SetObjectVariableInt

## Description
Sets the value of a VectorWorks object property. Used with properties requiring an INTEGER value.

For specific object selector index values, see the [Script Appendix](../Appendix/pages/Appendix%20G%20-%20Object%20Selectors.md).

```pascal
PROCEDURE SetObjectVariableInt(
				h     : HANDLE;
				index : INTEGER;
				value : INTEGER);
```

```python
def vs.SetObjectVariableInt(h, index, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|
|value|INTEGER|New value for property.|

## Examples
#### VectorScript ####
```pascal
SetObjectVariableInt(h,1,2);
```
#### Python ####
```python

```

```pascal
		{set Callout object text size}
		SetObjectVariableReal( CNH , 17, GetTextSize( textFoundH, 1 ) * (25.4/72.0));
		{set Callout object text style}
		SetObjectVariableInt( CNH , 19, GetTextStyle( textFoundH, 1 ) );
		{set Callout object font}
		SetObjectVariableInt( CNH , 28, GetTextFont( textFoundH, 1 ) );
END;

BEGIN
		DefaultWSFontID := GetObjectVariableInt(tempHandle,86);
		SetWSPlacement(tempHandle,130,223,698,816);
		{SetObjectVariableInt(tempHandle,86,0);} {Don't do this!!!!}
		SetObjectVariableInt(tempHandle,87,10);
		{Column Widths}
		SetWSColumnWidth(tempHandle,1,1,80);
		SetWSColumnWidth(tempHandle,2,2,96);
		SetWSColumnWidth(tempHandle,3,3,304);

		SetObjectVariableInt (gPluginH, 19, p__textStyle);
		SetObjectVariableInt (gPluginH, 28, p__textFont);
		gPenSize := kMarginLW;
		SetLW (gPluginH, gPenSize);
{
```
```python
vs.SetObjectVariableInt(h, 1, value)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
