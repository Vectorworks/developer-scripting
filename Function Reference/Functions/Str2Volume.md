# Str2Volume

## Description
Convert a string representation of a volume value to a real number in cubic millimeters.

```pascal
FUNCTION Str2Volume(str : STRING): REAL;
```

```python
def vs.Str2Volume(str):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|str|STRING|The string representation of the angle value.|

## Examples
```pascal
resultVal := Str2Volume('Example');
```
```python
import vs

# Convert a string representation of a volume value to a real number in cubic
# millimeters.
str = 'Example'

vol = vs.Str2Volume(str)
vs.Message('Str2Volume returned: ' + str(vol))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Strings](../Categories/Strings.md)
