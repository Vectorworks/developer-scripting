# GetObjectVariableInt

## Description
Returns the value of a VectorWorks object property. Used with properties returning an INTEGER value.

For specific object selector index values, see the [Script Appendix](../Appendix/pages/Appendix%20G%20-%20Object%20Selectors.md).

```pascal
FUNCTION GetObjectVariableInt(
				h     : HANDLE;
				index : INTEGER): INTEGER;
```

```python
def vs.GetObjectVariableInt(h, index):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|

## Examples
[ComplexDialogLayout4](examples/ComplexDialogLayout4.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
