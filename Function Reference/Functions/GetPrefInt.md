# GetPrefInt

## Description
Function GetPrefInt returns the value of a numeric VectorWorks preference setting.

A table of preference dialog items and their corresponding IDs may be found in the [[VS:Function Reference Appendix#Appendix F - Preference Selectors|Appendix]].

```pascal
FUNCTION GetPrefInt(prefIndex : INTEGER): INTEGER;
```

```python
def vs.GetPrefInt(prefIndex):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|prefIndex|INTEGER|Preference item constant.|

## Remarks
Returns the status of the specified preference item.  Used for preferences that return an Integer instead of a Boolean (see GetPref)

## Examples
==== VectorScript ====
```pascal
maxUndos:=GetPrefInt(17);
```
==== Python ====
```python
maxUndos = vs.GetPrefInt(17)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
