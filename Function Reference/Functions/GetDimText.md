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

```pascal
resultStr := GetDimText(h);
```
```python
import vs

# Function GetDimText returns the dimension value displayed with the
# referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

text = vs.GetDimText(h)
vs.Message('GetDimText returned: ' + str(text))
```

## Version
Availability: from All Versions

## Category
* [Dimensions](../Categories/Dimensions.md)
