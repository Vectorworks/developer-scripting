# SetPrefLongInt

## Description
Sets the value of the specified VectorWorks preference setting. Used with preference settings requiring a LONGINT value.

A table of preference dialog items and their corresponding IDs may be found in the [[VS:Function Reference Appendix#Appendix F - Preference Selectors|Appendix]].

```pascal
PROCEDURE SetPrefLongInt(
				index : INTEGER;
				value : LONGINT);
```

```python
def vs.SetPrefLongInt(index, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|Preference item index.|
|value|LONGINT|New value for preference.|

## Remarks
Sets the value of the specified preference to the value passed.   Similar to SetPref() except it works on preferences for long integer values

## Examples
#### VectorScript ####
```pascal
SetPrefLongInt(55,128);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks9.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
