# GetPrefLongInt

## Description
Returns the value of a VectorWorks preference setting. Used with preference settings returning a LONGINT value.

A table of preference dialog items and their corresponding IDs may be found in the [Scirpt Appendix](../Appendix/pages/Appendix%20F%20-%20Preference%20Selectors.md).

```pascal
FUNCTION GetPrefLongInt(prefIndex : INTEGER): LONGINT;
```

```python
def vs.GetPrefLongInt(prefIndex):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|prefIndex|INTEGER|Preference item index.|

## Remarks
Returns the status of the specified preference item.  Used for preferences that return a long integer instead of a Boolean (see GetPref)

The status of the requested preference. If the preference is a checkbox, then GetPrefLongInt returns TRUE or false. If it is a radio group or editable text item, then GetPrefLongInt returns an integer value representing that setting.

## Examples
#### VectorScript ####
```pascal
convertRes2D:= GetPrefLongInt(55);
```
#### Python ####
```python
convertRes2D = vs.GetPrefLongInt(55)
```

```pascal
BEGIN
	SetRField (objHand, objName, paramName, Num2Str (GetPrefLongInt (162), paramValue));
	alertMsg := Concat (locParamName, str1, Num2Str (GetPrefLongInt (162), lowerLimit), str2, Num2Str (GetPrefLongInt (169), upperLimit));
END

CASE gTagIdx OF
	4,7: gTagstr := concat(gTagstr,chr(13));
	END; {of CASE}
CASE gTagIdx OF
	3,4,6,7: gTagstr := concat(gTagstr,GetpluginString(3000),num2str(getpreflongint(179),gArea),getprefstring(178));
	END; {of CASE}
TextOrigin(pControlPoint01X,pControlPoint01Y);
CreateText(gTagstr);
gTextH := lnewobj;

BEGIN
	dec_prec := 1 / (10 ^ GetPrefLongInt(169));
	frac_prec := 1 / (2 ^ GetPrefLongInt(171));
	GetRoundingBase(display, primary, secondary);
	IF display = 1 THEN dec_prec := dec_prec * 2.5 ELSE
	IF display = 2 THEN dec_prec := dec_prec * 5;
```
```python
import vs

# Returns the value of a VectorWorks preference setting.
prefIndex = 1

resultN = vs.GetPrefLongInt(prefIndex)
vs.Message('GetPrefLongInt returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks9.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
