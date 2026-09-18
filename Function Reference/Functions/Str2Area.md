# Str2Area

## Description
Convert a string representation of an area value to a real number in square millimeters.

```pascal
FUNCTION Str2Area(str : STRING): REAL;
```

```python
def vs.Str2Area(str):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|str|STRING|The string representation of the area value.|

## Examples
```pascal
resultVal := Str2Area('Example');
```
```python
import vs

# Convert a string representation of an area value to a real number in square
# millimeters.
str = 'Example'

area = vs.Str2Area(str)
vs.Message('Str2Area returned: ' + str(area))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Strings](../Categories/Strings.md)
