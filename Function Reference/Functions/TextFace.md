# TextFace

## Description
Procedure TextFace sets the active text style of a VectorWorks document.

The text style may be one or a combination of the available styles, and should be enclosed in brackets. To specify multiple styles, each style should be separated by a comma.

```pascal
PROCEDURE TextFace(s : TEXTSTYLE);
```

```python
def vs.TextFace(s):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|s|TEXTSTYLE|Style setting for document.|

## Remarks
Make sure the docs indicate that the face must appear in set notation - check it out [PCP]

## Examples
#### VectorScript ####
```pascal
TextFace([Italic]);
{set the active text style to Italic}

TextFace([Bold,Outline]);
{set the active text style to bold outline}
```
#### Python ####
```python

```

```pascal
BEGIN
	TextSize(txtSize);
	CASE textStyleIndex OF
		1: TextFace([Bold]);
		2: TextFace([Italic]);
		3: TextFace([Bold,Italic]);
		OTHERWISE TextFace([]);
	END;	{of CASE textStyleIndex}

	IF styleIndex = 2 THEN fieldVal := GetLocStr(11002, 3) ELSE {Italic}
	IF styleIndex = 3 THEN fieldVal := GetLocStr(11002, 4);     {Bold Italic}
	SetRField(parmH, parmN, fieldN, fieldVal);
end else IF fieldVal <> '' THEN BEGIN
	IF fieldVal = GetLocStr(11002, 1) THEN BEGIN styleIndex := 0; TextFace([]);            end ELSE {Plain}
	IF fieldVal = GetLocStr(11002, 2) THEN BEGIN styleIndex := 1; TextFace([Bold]);        end ELSE {Bold}
	IF fieldVal = GetLocStr(11002, 3) THEN BEGIN styleIndex := 2; TextFace([Italic]);      end ELSE {Italic}
	IF fieldVal = GetLocStr(11002, 4) THEN BEGIN styleIndex := 3; TextFace([Bold,Italic]); END;     {Bold Italic}
	SetObjectVariableInt(parmH, 19, styleIndex);

BEGIN
	if Face = '0' then TextFace([]) ELSE
	if Face = '1' then TextFace([Bold]) ELSE
	if Face = '2' then TextFace([Italic]) ELSE
	if Face = '3' then TextFace([Bold,Italic]) ELSE
	if Face = '4' then TextFace([Underline]) ELSE
	if Face = '5' then TextFace([Bold,Underline]) ELSE
	if Face = '6' then TextFace([Italic,Underline]) ELSE
	IF Face = '7' THEN TextFace([Bold,Italic,Underline]);
END;
```
```python
vs.TextFace(s)
```

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
