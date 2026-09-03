# wsEditBeginN

## Description
Begin workspace edit. Use the other wsEdit* calls and must end with a call to wsEditEnd.

```pascal
PROCEDURE wsEditBeginN(
				companyName                : STRING;
				companyToolSetIconFilePath : STRING);
```

```python
def vs.wsEditBeginN(companyName, companyToolSetIconFilePath):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|companyName|STRING|   |
|companyToolSetIconFilePath|STRING|   |

## Examples
```pascal
wsEditBeginN('Example', 'file.txt');
```
```python
import vs

# Begin workspace edit.
companyName = 'Example'
companyToolSetIconFilePath = 'C:/Temp'

vs.wsEditBeginN(companyName, companyToolSetIconFilePath)
```

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
