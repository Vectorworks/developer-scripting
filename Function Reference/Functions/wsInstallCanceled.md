# wsInstallCanceled

## Description
This function must be called inside 'add_to_workspace' script and it will mark the install as canceled, interrupting the install.

```pascal
PROCEDURE wsInstallCanceled(canceled : BOOLEAN);
```

```python
def vs.wsInstallCanceled(canceled):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|canceled|BOOLEAN|   |

## Examples
```pascal
wsInstallCanceled(TRUE);
```
```python
import vs

# This function must be called inside 'add_to_workspace' script and it will
# mark the install as canceled, interrupting the install.
canceled = True

vs.wsInstallCanceled(canceled)
```

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
