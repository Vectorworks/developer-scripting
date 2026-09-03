# GetWallPrefStyle

## Description
Gets the name of the current document default wall style

```pascal
FUNCTION GetWallPrefStyle : STRING;
```

```python
def vs.GetWallPrefStyle():
    return STRING
```

## Remarks
Gets the name of the current document default wall style

## Examples
```pascal
resultStr := GetWallPrefStyle;
```
```python
import vs

# Gets the name of the current document default wall style.
text = vs.GetWallPrefStyle()
vs.Message('GetWallPrefStyle returned: ' + str(text))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
