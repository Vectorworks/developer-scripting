# GetPrefReal

## Description
Returns the value of a VectorWorks preference setting. Used with preference settings returning a REAL value.

A table of preference dialog items and their corresponding IDs may be found in the [Scirpt Appendix](../Appendix/pages/Appendix%20F%20-%20Preference%20Selectors.md).

```pascal
FUNCTION GetPrefReal(prefIndex : INTEGER): REAL;
```

```python
def vs.GetPrefReal(prefIndex):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|prefIndex|INTEGER|Preference item index.|

## Remarks
Returns the status of the specified preference item.  Used for preferences that return a real instead of a Boolean (see GetPref)

## Examples
#### VectorScript ####
```pascal
upi:= GetPrefReal(152);
```
#### Python ####
```python
upi = vs.GetPrefReal(152)
```

```pascal
BEGIN
	PushAttrs;
	recordName := GetName (recordH);
	upi := GetPrefReal (152);

recordName := GetName (recordH);
upi := GetPrefReal (152);

BEGIN {** Main ** }
	IF ResourceIsOK THEN InitConsts;
	UPI := GetPrefReal(kUPIPrefID);
```
```python
import vs

# Returns the value of a VectorWorks preference setting.
prefIndex = 1

value = vs.GetPrefReal(prefIndex)
vs.Message('GetPrefReal returned: ' + str(value))
```

## Version
Availability: from VectorWorks9.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
