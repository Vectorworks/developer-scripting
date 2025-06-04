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

## Version
Availability: from VectorWorks12.5

## Category
* [Command](../Categories/Command.md)
