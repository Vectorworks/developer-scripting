# RunNewColorPalette

## Description
Runs the New Color Palette Dialog

```pascal
FUNCTION RunNewColorPalette : STRING;
```

```python
def vs.RunNewColorPalette():
    return STRING
```

## Examples
```pascal
resultStr := RunNewColorPalette;
```
```python
import vs

# Runs the New Color Palette Dialog.
text = vs.RunNewColorPalette()
vs.Message('RunNewColorPalette returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2013

## Category
* [Color](../Categories/Color.md)
