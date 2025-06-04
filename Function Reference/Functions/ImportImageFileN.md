# ImportImageFileN

## Description
Import the specified image file as an Image object in Vectorworks. This function allows controlling the options when importing the image.

```pascal
FUNCTION ImportImageFileN(
				filePath : DYNARRAY[] of CHAR;
				importPt : REAL;
				mode     : INTEGER): HANDLE;
```

```python
def vs.ImportImageFileN(filePath, importPt, mode):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|filePath|DYNARRAY[] of CHAR|Import file path.|
|importPt|REAL|The import location.|
|mode|INTEGER|Import mode: 0 - import using import option dialog; 1 - import using the last options. If the call was never made with option dialog, then the first time it will show the options dialog.|

## See Also
VS Functions:
[ImportImageFile](ImportImageFile.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Utility](../Categories/Utility.md)
