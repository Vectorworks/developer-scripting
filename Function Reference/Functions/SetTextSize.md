# SetTextSize

## Description
Procedure SetTextSize sets the text size of a specified substring in the referenced text object. Parameters Start and Count specify the substring start position and substring length. Parameter Size specifies the size (in points) to be assigned to the substring.

```pascal
PROCEDURE SetTextSize(
				objectHd : HANDLE;
				Start    : INTEGER;
				Count    : INTEGER;
				Size     : REAL);
```

```python
def vs.SetTextSize(objectHd, Start, Count, Size):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to text object.|
|Start|INTEGER|Start position in text string.|
|Count|INTEGER|Length of substring.|
|Size|REAL|Text size setting for substring.|

## Remarks
The size parameter was previously an integer, but is now a floating point value. [9/14/98 - PCP]

## Examples
#### VectorScript ####
```pascal
SetTextSize(HandleToText,0,5,24);
{set the first five characters of the referenced text string to 24 point text}
```
#### Python ####
```python

```

```pascal
IF not ValidNumStr( GetText( textFoundH ), t_real ) THEN BEGIN
	TextOrigin(0,0);
	CreateText(Concat(' ', KNNoteNo));
	SetTextFont( LNewObj, 0, GetTextLength( LNewObj )-1 , GetTextFont( textFoundH, 0 ) );
	SetTextSize( LNewObj, 0, GetTextLength( LNewObj )-1 , GetTextSize( textFoundH, 0 ) );
	SetTextStyle( LNewObj, 0, GetTextLength( LNewObj )-1 , GetTextStyle( textFoundH, 0 ) );
	AddNumberWidth := GetTextWidth( LNewObj );
	DelObject(LNewObj);
end ELSE AddNumberWidth := 0;

	settextstyle(texthandle, 0, pos1, labelStyleIndex);
	settextsize (texthandle, 0, pos1, pLFact*TextScale * str2num(pTSize));
	settextstyle(texthandle, pos1, pos2-pos1+1, textStyleindex);
{
	labelFlag := TRUE;
	startpt := 0;

BEGIN
txtSize := GetTextSize(TmpTextHand,1);
txtSize := txtSize*(gTextSheetScale/100);
IF (gTextStyle = gsItemoverSheet) | (gTextStyle = gsItemSheet) THEN
	SetTextSize(TmpTextHand,(Len(txtStr)-Len(gSheetName)),Len(gSheetName),txtSize)
ELSE
	SetTextSize(TmpTextHand,0,Len(gSheetName),txtSize);
END;
```
```python
vs.SetTextSize(objectHd, Start, 1, 1.0)
```

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
