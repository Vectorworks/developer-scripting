# GetFPathName

## Description
Returns the fully-qualified filename of the active document.

```pascal
FUNCTION GetFPathName : STRING;
```

```python
def vs.GetFPathName():
    return STRING
```

## Examples
```pascal
resultStr := GetFPathName;
```
```python
import vs

# Returns the fully-qualified filename of the active document.
name = vs.GetFPathName()
vs.Message('GetFPathName returned: ' + str(name))
```

## Version
Availability: from Vectorworks 2014

## Category
* [File I@O](../Categories/File%20IO.md)
