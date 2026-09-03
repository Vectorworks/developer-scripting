# GetDLCompPenStylesN

## Description
Gets the left and right side pen styles of the component at index in the Double Line Preferences.

```pascal
FUNCTION GetDLCompPenStylesN(
				index             : INTEGER;
				VAR penStyleLeft  : LONGINT;
				VAR penStyleRight : LONGINT): BOOLEAN;
```

```python
def vs.GetDLCompPenStylesN(index):
    return (BOOLEAN, penStyleLeft, penStyleRight)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|penStyleLeft|LONGINT|Returns the pen style of the component's left line.  Positive values for patters, negative values for line types.|
|penStyleRight|LONGINT|Returns the pen style of the component's right line.  Positive values for patterns, negative values for line types.|

## Examples
```pascal
resultOK := GetDLCompPenStylesN(1, 2, 3);
```
```python
import vs

# Gets the left and right side pen styles of the component at index in the
# Double Line Preferences.
index = 1

ok, penStyleLeft, penStyleRight = vs.GetDLCompPenStylesN(index)
vs.Message('GetDLCompPenStylesN returned: ' + str((ok, penStyleLeft, penStyleRight)))
```

## See Also
VS Functions:
[SetDLCompPenStylesN](SetDLCompPenStylesN.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Document Settings](../Categories/Document%20Settings.md)
