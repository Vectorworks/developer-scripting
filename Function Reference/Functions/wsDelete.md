# wsDelete

## Description
Delete all menu commands and tools under the specified 'companyName' added with 'wsEditBegin'.

```pascal
PROCEDURE wsDelete(
				companyName : STRING;
				restart     : BOOLEAN;
				reload      : BOOLEAN);
```

```python
def vs.wsDelete(companyName, restart, reload):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|companyName|STRING|   |
|restart|BOOLEAN|   |
|reload|BOOLEAN|   |

## Examples
```pascal
wsDelete('Example', TRUE, FALSE);
```
```python
import vs

# Delete all menu commands and tools under the specified 'companyName' added
# with 'wsEditBegin'.
companyName = 'Example'
restart = True
reload = True

vs.wsDelete(companyName, restart, reload)
```

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
