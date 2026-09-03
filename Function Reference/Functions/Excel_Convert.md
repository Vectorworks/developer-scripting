# Excel_Convert

## Description
Convert Excel file to tab delimited text file.

```pascal
FUNCTION Excel_Convert(FilePath : STRING): STRING;
```

```python
def vs.Excel_Convert(FilePath):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|FilePath|STRING|   |

## Examples
```pascal
gUserImportFilePath := gImportFilePath;
gImportFilePath := Excel_Convert(gUserImportFilePath);
```
```python
import vs

# Convert Excel file to tab delimited text file.
FilePath = 'C:/Temp'

text = vs.Excel_Convert(FilePath)
vs.Message('Excel_Convert returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
