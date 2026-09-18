# ResList_IsSelValid

## Description
Determine if the selection in the popup is valid. The 'uniqueID' is a string identifier uniquely identifying this control.

```pascal
FUNCTION ResList_IsSelValid(uniqueID : STRING): BOOLEAN;
```

```python
def vs.ResList_IsSelValid(uniqueID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |

## Examples
```pascal
resultOK := ResList_IsSelValid('Example');
```
```python
import vs

# Determine if the selection in the popup is valid.
uniqueID = 'Example'

ok = vs.ResList_IsSelValid(uniqueID)
if ok:
    vs.Message('ResList_IsSelValid succeeded')
else:
    vs.Message('ResList_IsSelValid failed')
```

## Version
Availability: from Vectorworks 2017

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
