# GetFileSize

```pascal
FUNCTION GetFileSize(VAR FilePath : STRING): LONGINT;
```

```python
def vs.GetFileSize(FilePath):
    return (LONGINT, FilePath)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|FilePath|STRING|   |

## Examples
```pascal
{prepare progress dialog}
kProgressDlgStr := GetPlugInString(6012);
ProgressDlgOpen( kProgressDlgStr, FALSE );
ProgressDlgStart( 100.0, GetFileSize (gImportFilePath) );
```
```python
import vs

FilePath = 'C:/Temp'

resultN, FilePath = vs.GetFileSize(FilePath)
vs.Message('GetFileSize returned: ' + str((resultN, FilePath)))
```

## Version
Availability: from Vectorworks 2017

## Category
* [File I@O](../Categories/File%20IO.md)
