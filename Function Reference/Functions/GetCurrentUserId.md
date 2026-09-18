# GetCurrentUserId

## Description
Get the user id for the current user.

```pascal
FUNCTION GetCurrentUserId(VAR userid : STRING): BOOLEAN;
```

```python
def vs.GetCurrentUserId():
    return (BOOLEAN, userid)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|userid|STRING|   |

## Examples
```pascal
resultOK := GetCurrentUserId('Example');
```
```python
import vs

# Get the user id for the current user.
ok, userid = vs.GetCurrentUserId()
vs.Message('GetCurrentUserId returned: ' + str((ok, userid)))
```

## Version
Availability: from Vectorworks 2016

## Category
* [Project Sharing](../Categories/Project%20Sharing.md)
