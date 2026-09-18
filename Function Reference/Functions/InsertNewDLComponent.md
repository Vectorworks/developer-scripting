# InsertNewDLComponent

## Description
Inserts a new component before index in the Double Line Preferences.

```pascal
FUNCTION InsertNewDLComponent(
				beforeIndex    : INTEGER;
				widthDistance  : REAL;
				fill           : LONGINT;
				penWeightLeft  : INTEGER;
				penWeightRight : INTEGER;
				penStyleLeft   : INTEGER;
				penStyleRight  : INTEGER): BOOLEAN;
```

```python
def vs.InsertNewDLComponent(beforeIndex, widthDistance, fill, penWeightLeft, penWeightRight, penStyleLeft, penStyleRight):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|beforeIndex|INTEGER|The index before which to insert the new component.|
|widthDistance|REAL|The width of the component.|
|fill|LONGINT|The fill of the component.  Positive values for patterns, negative ref numbers for hatches.|
|penWeightLeft|INTEGER|The pen weight of the component's left line.|
|penWeightRight|INTEGER|The pen weight of the component's right line.|
|penStyleLeft|INTEGER|The pen style of the component's left line.  Positive values for patterns, negative values for dash styles.|
|penStyleRight|INTEGER|The pen style of the component's right line.  Positive values for patterns, negative values for dash styles.|

## Remarks
(6-27-06 CJG)

## Examples
```pascal
resultOK := InsertNewDLComponent(1, 1.0, 2, 3, 10, 5, 1);
```
```python
import vs

# Inserts a new component before index in the Double Line Preferences.
beforeIndex = 1
widthDistance = 2.0
fill = 1
penWeightLeft = 2
penWeightRight = 3
penStyleLeft = 0
penStyleRight = 0

ok = vs.InsertNewDLComponent(beforeIndex, widthDistance, fill, penWeightLeft, penWeightRight, penStyleLeft, penStyleRight)
if ok:
    vs.Message('InsertNewDLComponent succeeded')
else:
    vs.Message('InsertNewDLComponent failed')
```

## See Also
VS Functions:
[DeleteDLComponent](DeleteDLComponent.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Document Settings](../Categories/Document%20Settings.md)
