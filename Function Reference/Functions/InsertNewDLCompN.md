# InsertNewDLCompN

## Description
Inserts a new component before index in the Double Line Preferences.

```pascal
FUNCTION InsertNewDLCompN(
				beforeIndex    : INTEGER;
				widthDistance  : REAL (Coordinate);
				fill           : LONGINT;
				penWeightLeft  : INTEGER;
				penWeightRight : INTEGER;
				penStyleLeft   : LONGINT;
				penStyleRight  : LONGINT): BOOLEAN;
```

```python
def vs.InsertNewDLCompN(beforeIndex, widthDistance, fill, penWeightLeft, penWeightRight, penStyleLeft, penStyleRight):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|beforeIndex|INTEGER|The index before which to insert the new component.|
|widthDistance|REAL (Coordinate)|The width of the component.|
|fill|LONGINT|The fill of the component.  Positive values for patterns, negative ref numbers for hatches.|
|penWeightLeft|INTEGER|The pen weight of the component's left line.|
|penWeightRight|INTEGER|The pen weight of the component's right line.|
|penStyleLeft|LONGINT|The pen style of the component's left line.  Positive values for patterns, negative values for line types.|
|penStyleRight|LONGINT|The pen style of the component's right line.  Positive values for patterns, negative values for line types.|

## See Also
VS Functions:
[DeleteDLComponent](DeleteDLComponent.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Document Settings](../Categories/Document%20Settings.md)
