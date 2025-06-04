# GetPref

## Description
Function GetPref returns the on-off status of the specified preference item.

A table of preference dialog items and their corresponding IDs may be found in the [[VS:Function Reference Appendix#Appendix F - Preference Selectors|VectorScript Appendix]].

```pascal
FUNCTION GetPref(prefIndex : INTEGER): BOOLEAN;
```

```python
def vs.GetPref(prefIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|prefIndex|INTEGER|Preference item constant.|

## Examples
==== VectorScript ====
```pascal
SelHandleStatus:=GetPref(17);
```
Example for a shortcut to toggle preference true/false:
```pascal
SetPref(49,not GetPref(49));
```
==== Python ====
```python
SelHandleStatus = vs.GetPref(17)
```

## See Also
[SetPref](SetPref.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
