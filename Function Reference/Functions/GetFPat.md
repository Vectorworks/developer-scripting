# GetFPat

## Description
Function GetFPat returns the fill pattern of the referenced object.

A positive value corresponds to the index of the fill pattern on the pattern palette. A negative value corresponds to internal index of a vector fill pattern applied to the object.

Fill patterns and their associated constants can be found in the [[VS:Function Reference Appendix#Fill Patterns|VectorScript Appendix]].

```pascal
FUNCTION GetFPat(h : HANDLE): LONGINT;
```

```python
def vs.GetFPat(h):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
The negative values need to be converted to positive values for Index2Name to work.

## Examples
==== VectorScript ====
```pascal
FPatValue:=GetFPat(HandleToObj);
```
==== Python ====
```python
FPatValue = vs.GetFPat(HandleToObj)
```

## Version
Availability: from All Versions

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
