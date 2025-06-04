# SetClOpacity

## Description
Sets the opacity persentage of a class. The opacity is specified by percentage value in range [0-100].

```pascal
PROCEDURE SetClOpacity(
				className : STRING;
				opacity   : INTEGER);
```

```python
def vs.SetClOpacity(className, opacity):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|opacity|INTEGER|Opacity specified by percentage value in range [0-100].|

## Examples
==== VectorScript ====
```pascal
ColorIndexToRGB(214,cRed,cGrn,cBlu);
SetClOpacity('Cold Water Supply',cRed,cGrn,cBlu);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks13.0

## Category
* [Classes](../Categories/Classes.md)
