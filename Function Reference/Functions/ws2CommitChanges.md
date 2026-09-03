# ws2CommitChanges

## Description
Workspace advanced APIs. Offers restart or reload of the workspace to commit the changes made by this APIs.

```pascal
PROCEDURE ws2CommitChanges(
				restart : BOOLEAN;
				reload  : BOOLEAN);
```

```python
def vs.ws2CommitChanges(restart, reload):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|restart|BOOLEAN|   |
|reload|BOOLEAN|   |

## Examples
```pascal
ws2CommitChanges(TRUE, FALSE);
```
```python
import vs

# Workspace advanced APIs.
restart = True
reload = True

vs.ws2CommitChanges(restart, reload)
```

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
