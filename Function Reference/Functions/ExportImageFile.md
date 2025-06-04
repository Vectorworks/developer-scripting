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

## Version
Availability: from Vectorworks 2015

## Category
* [Utility](../Categories/Utility.md)
