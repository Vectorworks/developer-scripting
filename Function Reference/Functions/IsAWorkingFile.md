# IsAWorkingFile

## Description
Returns True if the current document is a Project Sharing Working File. Otherwise returns False.

```pascal
FUNCTION IsAWorkingFile : BOOLEAN;
```

```python
def vs.IsAWorkingFile():
    return BOOLEAN
```

## Examples
```pascal
resultOK := IsAWorkingFile;
```
```python
import vs

# Returns True if the current document is a Project Sharing Working File.
ok = vs.IsAWorkingFile()
if ok:
    vs.Message('IsAWorkingFile succeeded')
else:
    vs.Message('IsAWorkingFile failed')
```

## Version
Availability: from Vectorworks 2016

## Category
* [Project Sharing](../Categories/Project%20Sharing.md)
