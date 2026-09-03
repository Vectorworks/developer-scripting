# ExportPDFPages

## Description
This will export the current document to PDF.  You must call OpenPDFDocument before calling this function.  This is intended to support Batch Export to PDF.

```pascal
FUNCTION ExportPDFPages(savedViewNameStr : STRING): INTEGER;
```

```python
def vs.ExportPDFPages(savedViewNameStr):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|savedViewNameStr|STRING|   |

## Examples
```pascal
resultN := ExportPDFPages('Example');
```
```python
import vs

# This will export the current document to PDF.
savedViewNameStr = 'Example'

resultN = vs.ExportPDFPages(savedViewNameStr)
vs.Message('ExportPDFPages returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks12.5

## Category
* [Command](../Categories/Command.md)
