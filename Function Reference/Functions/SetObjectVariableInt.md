# SetObjectVariableInt

## Description
Sets the value of a VectorWorks object property. Used with properties requiring an INTEGER value.

For specific object selector index values, see the [Script Appendix](../Appendix/pages/Appendix%20G%20-%20Object%20Selectors.md).

```pascal
PROCEDURE SetObjectVariableInt(
				h     : HANDLE;
				index : INTEGER;
				value : INTEGER);
```

```python
def vs.SetObjectVariableInt(h, index, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|
|value|INTEGER|New value for property.|

## Examples
#### VectorScript ####
```pascal
SetObjectVariableInt(h,1,2);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
