# wsEditAddMenu

## Description
Add a menu under Tools -&gt; Thrid-party. Use dot as a delimiter for sub menus in 'commandName'.

```pascal
PROCEDURE wsEditAddMenu(menuPath : STRING);
```

```python
def vs.wsEditAddMenu(menuPath):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|menuPath|STRING|   |

## Remarks
(MaKro) Had no success with dot as delimiter. Slash works fine.

## Examples
```pascal
wsEditAddMenu('file.txt');
```
```python
import vs

# Add a menu under Tools -&gt; Thrid-party.
menuPath = 'C:/Temp'

vs.wsEditAddMenu(menuPath)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Workspaces](../Categories/Workspaces.md)
