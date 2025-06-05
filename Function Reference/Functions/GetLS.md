# GetLS

## Description
_Use [GetLSN](GetLSN.md) instead._
Function GetLS returns the line style of the referenced object.

```pascal
FUNCTION GetLS(h : HANDLE): INTEGER;
```

```python
def vs.GetLS(h):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
*_c_* 2016.02.29: This is deprecated and returns always -1 as of VW 2016.

## Examples
#### VectorScript ####
```pascal
lStyleValue := GetLS(handleToObject);
```
#### Python ####
```python
lStyleValue = vs.GetLS(handleToObject)
```

## See Also
[GetLSN|GetLSN](GetLSN|GetLSN.md) from Vectorworks 2013

## Version
Availability: from All Versions, deprecated from Vectorworks 2013

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
