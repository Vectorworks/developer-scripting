# SetObjectVariableString

## Description
Sets the value of a VectorWorks object property. Used with properties requiring a STRING value.

For specific object selector index values, see the [Script Appendix](../Appendix/pages/Appendix%20G%20-%20Object%20Selectors.md).

```pascal
PROCEDURE SetObjectVariableString(
				h     : HANDLE;
				index : INTEGER;
				value : STRING);
```

```python
def vs.SetObjectVariableString(h, index, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|
|value|STRING|New value for property.|

## Examples
#### VectorScript ####
```pascal
SetPref(17,FALSE);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
