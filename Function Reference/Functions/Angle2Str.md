# Angle2Str

## Description
Convert an angle value (in degrees) from a real number to a string using the current document formatting.

```pascal
FUNCTION Angle2Str(value : REAL): STRING;
```

```python
def vs.Angle2Str(value):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|value|REAL|The angle value in degrees.|

## Examples
```pascal
CASE kTextType+2*(j-1) OF
	kRealBA, kRealBA2, kRealFA, kRealFA2: BEGIN
		IF GetEditReal(dialogIDIMEdit, kTextType+2*(j-1), 2, choiceReal) THEN
			IF (selSize=1) | (choiceReal<>0) THEN
				boo:=SetLBItemInfo(dialogIDIM, kBrowser, i-1, j, Angle2Str(choiceReal), 0);
	END;
```
```python
import vs

# Convert an angle value (in degrees) from a real number to a string using
# the current document formatting.
value = 1.0

text = vs.Angle2Str(value)
vs.Message('Angle2Str returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Strings](../Categories/Strings.md)
