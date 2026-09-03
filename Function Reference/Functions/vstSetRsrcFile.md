# vstSetRsrcFile

## Description
Sets the name of the resource file containing mode bar buttons. For Industry Series products, this should always be the IP Resources file.

```pascal
PROCEDURE vstSetRsrcFile(inFileName : STRING);
```

```python
def vs.vstSetRsrcFile(inFileName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inFileName|STRING|   |

## Examples
```pascal
vstSetRsrcFile('file.txt');
```
```python
import vs

# Sets the name of the resource file containing mode bar buttons.
inFileName = 'C:/Temp/example.txt'

vs.vstSetRsrcFile(inFileName)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
