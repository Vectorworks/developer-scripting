# GetPrefString

## Description
Returns the value of a VectorWorks preference setting. Used with preference settings returning a STRING value.

A table of preference dialog items and their corresponding IDs may be found in the [Scirpt Appendix](../Appendix/pages/Appendix%20F%20-%20Preference%20Selectors.md).

```pascal
FUNCTION GetPrefString(prefIndex : INTEGER): STRING;
```

```python
def vs.GetPrefString(prefIndex):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|prefIndex|INTEGER|Preference item index.|

## Remarks
Returns the status of the specified preference item.  Used for preferences that return a string instead of a Boolean (see GetPref)

## Examples
#### VectorScript ####
```pascal
unitmark:=GetPrefString(154);
```
#### Python ####
```python
unitmark = vs.GetPrefString(154)
```

```pascal
{save the current text style, and font of the doc in order to restore them after the creation of the new callout}
oldDocFontName	:= GetPrefString(100);
oldDocFontStyle	:= GetPrefInt(58);

BEGIN
gHtUnitStr := GetPrefString(154);
IF gHtUnitStr='"' THEN gHtUnitStr:= ' in';
nomht := Concat(ht);{Num2StrF(PCustom_Height)}
END;

CASE GetPrefInt (170) OF
	1, 2: um := GetPluginString (5001);
	3   : um := GetPluginString (5002);
	OTHERWISE um := GetPrefString (154);
END;
```
```python
import vs

# Returns the value of a VectorWorks preference setting.
prefIndex = 1

text = vs.GetPrefString(prefIndex)
vs.Message('GetPrefString returned: ' + str(text))
```

## Version
Availability: from VectorWorks9.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
