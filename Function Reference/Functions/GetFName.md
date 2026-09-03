# GetFName

## Description
Function GetFName returns the current file name of the active document.

```pascal
FUNCTION GetFName : STRING;
```

```python
def vs.GetFName():
    return STRING
```

## Remarks
See also: [GetFPathName](GetFPathName.md), which returns the fully qualified path of the active document.

## Examples
```pascal
resultStr := GetFName;
```
```python
import vs

# Function GetFName returns the current file name of the active document.
name = vs.GetFName()
vs.Message('GetFName returned: ' + str(name))
```

## Version
Availability: from All Versions

## Category
* [Document Settings](../Categories/Document%20Settings.md)
