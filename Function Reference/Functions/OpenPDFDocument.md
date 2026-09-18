# OpenPDFDocument

## Description
Begins the export to a PDF document.  You must call AcquireExportPDFSettingsAndLocation before calling this function. This is intended to support Batch PDF Export.

```pascal
FUNCTION OpenPDFDocument(inFilenameStr : STRING): BOOLEAN;
```

```python
def vs.OpenPDFDocument(inFilenameStr):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inFilenameStr|STRING|   |

## Examples
```pascal
resultOK := OpenPDFDocument('file.txt');
```
```python
import vs

# Begins the export to a PDF document.
inFilenameStr = 'C:/Temp/example.txt'

ok = vs.OpenPDFDocument(inFilenameStr)
if ok:
    vs.Message('OpenPDFDocument succeeded')
else:
    vs.Message('OpenPDFDocument failed')
```

## Version
Availability: from VectorWorks12.5

## Category
* [Command](../Categories/Command.md)
