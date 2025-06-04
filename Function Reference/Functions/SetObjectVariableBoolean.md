# SetObjectVariableBoolean

## Description
Sets the ON-OFF status of a VectorWorks object property.

For specific object selector index values, see the [[VS:Function Reference Appendix#Appendix G - Object Selectors|Appendix]].

```pascal
PROCEDURE SetObjectVariableBoolean(
				h      : HANDLE;
				index  : INTEGER;
				status : BOOLEAN);
```

```python
def vs.SetObjectVariableBoolean(h, index, status):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|
|status|BOOLEAN|New status for property.|

## Examples
==== VectorScript ====
```pascal
SetObjectVariableBoolean(obj, 17, FALSE);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks 9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
