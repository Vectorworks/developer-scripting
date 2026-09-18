# wsEditBegin

## Description
Begin workspace edit. Use the other workspaceEdit* calls and must end with a call to workspaceEditEnd.

```pascal
PROCEDURE wsEditBegin(companyName : STRING);
```

```python
def vs.wsEditBegin(companyName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|companyName|STRING|   |

## Examples
```pascal
wsEditBegin('Example');
```
```python
import vs

# Begin workspace edit.
companyName = 'Example'

vs.wsEditBegin(companyName)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Workspaces](../Categories/Workspaces.md)
