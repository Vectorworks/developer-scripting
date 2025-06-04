# SetDLCompPenStylesN

## Description
Sets the left and right pen styles for the component at index in the Double Line Preferences.

```pascal
FUNCTION SetDLCompPenStylesN(
				index         : INTEGER;
				penStyleLeft  : LONGINT;
				penStyleRight : LONGINT): BOOLEAN;
```

```python
def vs.SetDLCompPenStylesN(index, penStyleLeft, penStyleRight):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|penStyleLeft|LONGINT|The pen style of the component's left line.  Positive values for patterns, negative values for line types.|
|penStyleRight|LONGINT|The pen style of the component's right line.  Positive values for patterns, negative values for line types.|

## See Also
VS Functions:
[GetDLCompPenStylesN](GetDLCompPenStylesN.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Document Settings](../Categories/Document%20Settings.md)
