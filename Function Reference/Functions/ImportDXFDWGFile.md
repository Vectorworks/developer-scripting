# ImportDXFDWGFile

## Description
Import specific DXF/DWG file

```pascal
FUNCTION ImportDXFDWGFile(fileName : STRING): INTEGER;
```

```python
def vs.ImportDXFDWGFile(fileName):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fileName|STRING|   |

## Examples
```pascal
resultN := ImportDXFDWGFile('file.txt');
```
```python
import vs

# Import specific DXF/DWG file.
fileName = 'C:/Temp/example.txt'

resultN = vs.ImportDXFDWGFile(fileName)
vs.Message('ImportDXFDWGFile returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2013

## Category
* [ImportExport](../Categories/ImportExport.md)
