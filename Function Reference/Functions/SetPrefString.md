# SetPrefString

## Description
Sets the value of the specified VectorWorks preference setting. Used with preference settings requiring a STRING value.

A table of preference dialog items and their corresponding IDs may be found in the [Scirpt Appendix](../Appendix/pages/Appendix%20F%20-%20Preference%20Selectors.md).

```pascal
PROCEDURE SetPrefString(
				index : INTEGER;
				value : STRING);
```

```python
def vs.SetPrefString(index, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|Preference item index.|
|value|STRING|New value for preference.|

## Remarks
Sets the value of the specified preference to the value passed.   Similar to SetPref() except it works on preferences for string values

## Examples
#### VectorScript ####
```pascal
SetPrefString(154,'cubits');
```
#### Python ####
```python

```

```pascal
{set the text style, size and font for the creation of the new Callout}
SetPrefString(100, GetFontName(GetTextFont( textFoundH, 0 )) );
{SetPrefReal(57, GetTextSize(textFoundH, 0 ) );}
SetPrefInt(58, GetTextStyle( textFoundH, 0 ) );

txtJust := GetPrefInt(82);
txtVert := GetPrefInt(83);
SetPrefInt(82, 1);
SetPrefInt(83, 1);
SetPrefString(100, 'Arial Unicode MS');

gActivePane := GetActivePane(dialog1, kTabControl);
gActStringerPane := GetActivePane(dialog1, kStringersTabControl);
SetPrefString(100, defaultFont);
```
```python
vs.SetPrefString(1, value)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
