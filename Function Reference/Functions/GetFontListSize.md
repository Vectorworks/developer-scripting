# GetFontListSize

## Description
Returns the number of available fonts on the local system.

```pascal
FUNCTION GetFontListSize : INTEGER;
```

```python
def vs.GetFontListSize():
    return INTEGER
```

## Examples
```python
AlrtDialog(Concat('The number of available fonts is: ', GetFontListSize));
```

```pascal
resultN := GetFontListSize;
```
```python
import vs

# Returns the number of available fonts on the local system.
resultN = vs.GetFontListSize()
vs.Message('GetFontListSize returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
