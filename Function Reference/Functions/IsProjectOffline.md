# IsProjectOffline

## Description
Checks if current document is a Working File operating in Offline Mode.<BR>
<BR>
Offline Mode is when the Working File is opened and the Project File cannot be found.

```pascal
FUNCTION IsProjectOffline : BOOLEAN;
```

```python
def vs.IsProjectOffline():
    return BOOLEAN
```

## Examples
```pascal
resultOK := IsProjectOffline;
```
```python
import vs

# Checks if current document is a Working File operating in Offline Mode.
ok = vs.IsProjectOffline()
if ok:
    vs.Message('IsProjectOffline succeeded')
else:
    vs.Message('IsProjectOffline failed')
```

## Version
Availability: from Vectorworks 2016

## Category
* [Project Sharing](../Categories/Project%20Sharing.md)
