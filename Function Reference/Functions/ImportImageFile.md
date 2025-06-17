# ImportImageFile

## Description
Import the specified image file as an Image object in Vectorworks.

```pascal
FUNCTION ImportImageFile(
				filePath : DYNARRAY[] of CHAR;
				importPt : POINT): HANDLE;
```

```python
def vs.ImportImageFile(filePath, importPt):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|filePath|DYNARRAY[] of CHAR|Full path to the image file.|
|importPt|POINT|Location on which the file should be imported. You can pass X, Y REAL coordinates here instead of POINT.|

## Remarks
This function returns NIL in Vectorworks 2014.

A typical call to this function would be:
<code lang='py'>
hImage = vs.ImportImageFile( imagePath, importPt )
```

In Vectorworks 2014, if you need the result, the call should be:
<code lang='py'>
vs.ImportImageFile( imagePath, importPt )
hImage = vs.FSActLayer()
```

## Examples
[[Python Sample Import Images as Symbols]] for example.

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
