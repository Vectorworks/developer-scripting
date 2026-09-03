# GetProjectUser

## Description
For a given userid in the current Project, get their full name and permission level.<BR>

**Table - Project Sharing Permissions**

| Permission Level         | Constant |
|-------------------------|----------|
| Read Only               | 1        |
| Layers-Restricted       | 2        |
| Layers-Unrestricted     | 3        |
| Layers and Resources    | 4        |
| Project                 | 5        |
| Administrative          | 6        |

```pascal
FUNCTION GetProjectUser(
				userId         : STRING;
				VAR fullName   : STRING;
				VAR permission : INTEGER): BOOLEAN;
```

```python
def vs.GetProjectUser(userId):
    return (BOOLEAN, fullName, permission)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|userId|STRING|The userid to look up|
|fullName|STRING|The users full name|
|permission|INTEGER|Permission level of the user|

## Examples
```pascal
resultOK := GetProjectUser('Example', 'Example', 1);
```
```python
import vs

# For a given userid in the current Project, get their full name and
# permission level.
userId = 'Example'

ok, fullName, permission = vs.GetProjectUser(userId)
vs.Message('GetProjectUser returned: ' + str((ok, fullName, permission)))
```

## See Also
VS Functions:
[GetProjectUserNames](GetProjectUserNames.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Project Sharing](../Categories/Project%20Sharing.md)
