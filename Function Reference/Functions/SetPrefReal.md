# SetPrefReal

## Description
Sets the value of the specified VectorWorks preference setting. Used with preference settings requiring a REAL value.

A table of preference dialog items and their corresponding IDs may be found in the [[VS:Function Reference Appendix#Appendix F - Preference Selectors|Appendix]].

```pascal
PROCEDURE SetPrefReal(
				index : INTEGER;
				value : REAL);
```

```python
def vs.SetPrefReal(index, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|Preference item index.|
|value|REAL|New value for preference.|

## Remarks
Sets the value of the specified preference to the value passed.   Similar to SetPref() except it works on preferences for real values

## Examples
==== VectorScript ====
```pascal
SetPrefReal(68,144);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks9.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
