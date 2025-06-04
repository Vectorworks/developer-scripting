# GetObjectVariableInt

## Description
Returns the value of a VectorWorks object property. Used with properties returning an INTEGER value.

For specific object selector index values, see the [[VS:Function Reference Appendix#Appendix G - Object Selectors|Appendix]].

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
mplexDialogLayout4}}

## Version
Availability: from VectorWorks9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
