# GetDimText

## Description
Function GetDimText returns the dimension value displayed with the referenced object.

```pascal
FUNCTION GetDimText(h : HANDLE): STRING;
```

```python
def vs.GetDimText(h):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Examples
#### VectorScript ####
```pascal
DimValue:=GetDimText(HandleToObj);
```
#### Python ####
```python
DimValue =vs.GetDimText(HandleToObj)
```

## Version
Availability: from All Versions

## Category
* [Dimensions](../Categories/Dimensions.md)
