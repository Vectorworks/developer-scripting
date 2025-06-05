# SetPrefInt

## Description
Function SetPrefInt sets the value of a numeric VectorWorks preference setting.

A table of preference dialog items and their corresponding IDs may be found in the [Scirpt Appendix](../Appendix/pages/Appendix%20F%20-%20Preference%20Selectors.md).

```pascal
PROCEDURE SetPrefInt(
				index : INTEGER;
				value : INTEGER);
```

```python
def vs.SetPrefInt(index, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|Preference item constant.|
|value|INTEGER|New value for preference.|

## Remarks
Sets the value of the specified preference to the value passed.   Similar to SetPref() except it works on preferences for Integer values

## Examples
#### VectorScript ####
```pascal
SetPrefInt(17,FALSE);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks8.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
