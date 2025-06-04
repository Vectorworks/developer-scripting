# SetPrefString

## Description
Sets the value of the specified VectorWorks preference setting. Used with preference settings requiring a STRING value.

A table of preference dialog items and their corresponding IDs may be found in the [[VS:Function Reference Appendix#Appendix F - Preference Selectors|Appendix]].

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

## Version
Availability: from VectorWorks9.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
