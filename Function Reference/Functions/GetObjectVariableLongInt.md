# GetObjectVariableLongInt

## Description
Returns the value of a VectorWorks object property. Used with properties returning a LONGINT value.

For specific object selector index values, see the [[VS:Function Reference Appendix#Appendix G - Object Selectors|Appendix]].

```pascal
FUNCTION GetObjectVariableLongInt(
				h     : HANDLE;
				index : INTEGER): LONGINT;
```

```python
def vs.GetObjectVariableLongInt(h, index):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|

## Examples
==== VectorScript ====
```pascal
p:= GetObjectVariableLongInt(h,579);
```
==== Python ====
```python
p = vs.GetObjectVariableLongInt(h,579)
```

## Version
Availability: from VectorWorks9.0

## Category
* Object Info

