# Area2Str

## Description
Convert an area value (in square millimeters) from a real number to a string using the current document formatting.

```pascal
FUNCTION Area2Str(value : REAL): STRING;
```

```python
def vs.Area2Str(value):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|value|REAL|The area value in square millimeters|

## Examples
```pascal
resultStr := Area2Str(1.0);
```
```python
import vs

# Convert an area value (in square millimeters) from a real number to a
# string using the current document formatting.
value = 1.0

text = vs.Area2Str(value)
vs.Message('Area2Str returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Strings](../Categories/Strings.md)
