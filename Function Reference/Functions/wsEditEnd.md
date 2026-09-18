# wsEditEnd

## Description
Finishes workspace edit started with workspaceEditBegin.

```pascal
FUNCTION wsEditEnd(restart : BOOLEAN): BOOLEAN;
```

```python
def vs.wsEditEnd(restart):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|restart|BOOLEAN|   |

## Examples
```pascal
resultOK := wsEditEnd(TRUE);
```
```python
import vs

# Finishes workspace edit started with workspaceEditBegin.
restart = True

ok = vs.wsEditEnd(restart)
if ok:
    vs.Message('wsEditEnd succeeded')
else:
    vs.Message('wsEditEnd failed')
```

## Version
Availability: from Vectorworks 2018

## Category
* [Workspaces](../Categories/Workspaces.md)
