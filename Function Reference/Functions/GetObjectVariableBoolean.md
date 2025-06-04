# GetObjectVariableBoolean

## Description
Returns the ON-OFF status of a VectorWorks object property. 

For specific object selector index values, see the [[VS:Function Reference Appendix#Appendix G - Object Selectors|Appendix]].

```pascal
FUNCTION GetObjectVariableBoolean(
				h     : HANDLE;
				index : INTEGER): BOOLEAN;
```

```python
def vs.GetObjectVariableBoolean(h, index):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|

## Remarks
From Julian: Appears to be unreliable for walls because it returns a different result depending on the view. Walls always report false for 2D, but only report true for 3D if in a 3D view.

## Examples
==== VectorScript ====
```pascal
castShadow:= GetObjectVariableBoolean(h,53);
```
==== Python ====
```python
castShadow = vs.GetObjectVariableBoolean(h,53)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
