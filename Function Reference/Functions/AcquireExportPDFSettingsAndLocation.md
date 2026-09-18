# AcquireExportPDFSettingsAndLocation

## Description
Asks the user for the Export PDF settings and the PDF file name (or folder name if the parameter is true).  This is intended to support Batch PDF Export.

```pascal
FUNCTION AcquireExportPDFSettingsAndLocation(inbSeparateDocuments : BOOLEAN): BOOLEAN;
```

```python
def vs.AcquireExportPDFSettingsAndLocation(inbSeparateDocuments):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inbSeparateDocuments|BOOLEAN|   |

## Examples
```pascal
resultOK := AcquireExportPDFSettingsAndLocation(TRUE);
```
```python
import vs

# Asks the user for the Export PDF settings and the PDF file name (or folder
# name if the parameter is true).
inbSeparateDocuments = True

ok = vs.AcquireExportPDFSettingsAndLocation(inbSeparateDocuments)
if ok:
    vs.Message('AcquireExportPDFSettingsAndLocation succeeded')
else:
    vs.Message('AcquireExportPDFSettingsAndLocation failed')
```

## Version
Availability: from VectorWorks12.5

## Category
* [Command](../Categories/Command.md)
