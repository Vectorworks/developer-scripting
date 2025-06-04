# GetPrefLongInt

## Description
Returns the value of a VectorWorks preference setting. Used with preference settings returning a LONGINT value.

A table of preference dialog items and their corresponding IDs may be found in the [[VS:Function Reference Appendix#Appendix F - Preference Selectors|Appendix]].

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
==== VectorScript ====
```pascal
convertRes2D:= GetPrefLongInt(55);
```
==== Python ====
```python
convertRes2D = vs.GetPrefLongInt(55)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
