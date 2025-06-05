# GetObjectVariableReal

## Description
Returns the value of a VectorWorks object property. Used with properties returning a REAL value. Always returns values in mm, regardless of document units.

For specific object selector index values, see the [Script Appendix](../Appendix/pages/Appendix%20G%20-%20Object%20Selectors.md).

```pascal
FUNCTION GetObjectVariableReal(
				h     : HANDLE;
				index : INTEGER): REAL;
```

```python
def vs.GetObjectVariableReal(h, index):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|

## Examples
#### VectorScript ####
```pascal
dim_offset:= GetObjectVariableReal(h,4);
```
#### Python ####
```python
dim_offset = vs.GetObjectVariableReal(h,4)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
