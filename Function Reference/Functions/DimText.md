# DimText

## Description
Procedure DimText converts the most recently created line object in VectorScript to a dimension.

```pascal
PROCEDURE DimText;
```

```python
def vs.DimText():
    return None
```

## Remarks
Creates a linear dimension object from the last line object that was drawn using VectorScript.

## Examples
#### VectorScript ####
```pascal
LineTo(2,2);
DimText;
```
#### Python ####
```python
vs.LineTo(2,2)
vs.DimText()
```

## Version
Availability: from All Versions

## Category
* [Dimensions](../Categories/Dimensions.md)
