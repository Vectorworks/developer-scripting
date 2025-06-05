# SetObjectVariableBoolean

## Description
Sets the ON-OFF status of a VectorWorks object property.

For specific object selector index values, see the [Script Appendix](../Appendix/pages/Appendix%20G%20-%20Object%20Selectors.md).

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
#### VectorScript ####
```pascal
SetObjectVariableBoolean(obj, 17, FALSE);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks 9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
