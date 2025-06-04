# GetPrefString

## Description
Returns the value of a VectorWorks preference setting. Used with preference settings returning a STRING value.

A table of preference dialog items and their corresponding IDs may be found in the [[VS:Function Reference Appendix#Appendix F - Preference Selectors|Appendix]].

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
==== VectorScript ====
```pascal
unitmark:=GetPrefString(154);
```
==== Python ====
```python
unitmark = vs.GetPrefString(154)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
