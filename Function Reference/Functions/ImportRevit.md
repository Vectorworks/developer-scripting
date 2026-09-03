# ImportRevit

## Description
Import RVT and RFA files

```pascal
PROCEDURE ImportRevit(fileName : DYNARRAY[] of CHAR);
```

```python
def vs.ImportRevit(fileName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fileName|DYNARRAY[] of CHAR|   |

## Examples
```pascal
ImportRevit(fileName);
```
```python
import vs

# Import RVT and RFA files.
fileName = 'C:/Temp/example.txt'

vs.ImportRevit(fileName)
```

## Version
Availability: from Vectorworks 2017

## Category
* [ImportExport](../Categories/ImportExport.md)
