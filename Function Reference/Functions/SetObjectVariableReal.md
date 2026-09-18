# SetObjectVariableReal

## Description
Sets the value of a VectorWorks object property. Used with properties requiring a REAL value.

For specific object selector index values, see the [Script Appendix](../Appendix/pages/Appendix%20G%20-%20Object%20Selectors.md).

```pascal
PROCEDURE SetObjectVariableReal(
				h     : HANDLE;
				index : INTEGER;
				value : REAL);
```

```python
def vs.SetObjectVariableReal(h, index, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|
|value|REAL|New value for property.|

## Examples
#### VectorScript ####
```pascal
SetPref(17,FALSE);
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

BEGIN
	fieldstr := GetRField(parmH,parmN,fieldN);
	fieldval := Str2Num(fieldstr);
	IF (fieldval <> 0) THEN BEGIN
		SetObjectVariableReal(parmH,17,fieldval*factor*GetLScale(GetLayer(parmH)));{pts to world coords}
		SetRField(parmH,parmN,fieldN,'0');
		SetRField(parmH,parmN,'BubbleTSize',fieldstr);
	END;

if version >= 1000 then BEGIN
	fieldVal := GetObjectVariableReal(parmH, 17) * (72.0/25.4) / containerScale;
	SetRField(parmH, parmN, fieldN, Num2Str(3, fieldVal));
end else if (ValidNumStr(GetRField(parmH, parmN, fieldN), fieldVal)) & (fieldVal > 0) then BEGIN
	SetObjectVariableReal(parmH, 17, fieldVal * (25.4/72.0) * containerScale); {pts to world coords}
	TextSize(fieldVal);
END;
```
```python
vs.SetObjectVariableReal(h, 1, value)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
