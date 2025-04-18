# GetObjectVariableString

## Description
Returns the value of a VectorWorks object property. Used with properties returning a STRING value.

For specific object selector index values, see the [[VS:Function Reference Appendix#Appendix G - Object Selectors|Appendix]].

```pascal
FUNCTION GetObjectVariableString(
				h     : HANDLE;
				index : INTEGER): STRING;
```

```python
def vs.GetObjectVariableString(h, index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|

## Examples
==== VectorScript ====
```pascal
dimstdName:= GetObjectVariableString(h,27);
```
==== Python ====
```python
dimstdName = vs.GetObjectVariableString(h,27)
```

## Version
Availability: from VectorWorks9.0

## Category
* Object Info

