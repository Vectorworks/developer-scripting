# Str2Angle

## Description
Convert a string representation of an angle value to a real number in degrees.

```pascal
FUNCTION Str2Angle(str : STRING): REAL;
```

```python
def vs.Str2Angle(str):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|str|STRING|The string representation of the angle value.|

## Examples
```pascal
resultVal := Str2Angle('Example');
```
```python
import vs

# Convert a string representation of an angle value to a real number in degrees.
str = 'Example'

angle = vs.Str2Angle(str)
vs.Message('Str2Angle returned: ' + str(angle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Strings](../Categories/Strings.md)
