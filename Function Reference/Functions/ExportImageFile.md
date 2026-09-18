# ExportImageFile

## Description
Export the specified Image object in Vectorworks as an image file.

```pascal
FUNCTION ExportImageFile(
				hHmage   : HANDLE;
				filePath : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.ExportImageFile(hHmage, filePath):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hHmage|HANDLE|The handle of the image object to be exported.|
|filePath|DYNARRAY[] of CHAR|Full path to the output image file.|

## Examples
```pascal
resultOK := ExportImageFile(hHmage, filePath);
```
```python
import vs

# Export the specified Image object in Vectorworks as an image file.
hHmage = vs.FSActLayer()  # handle to the first selected object on the active layer
filePath = 'C:/Temp'

ok = vs.ExportImageFile(hHmage, filePath)
if ok:
    vs.Message('ExportImageFile succeeded')
else:
    vs.Message('ExportImageFile failed')
```

## Version
Availability: from Vectorworks 2015

## Category
* [Utility](../Categories/Utility.md)
