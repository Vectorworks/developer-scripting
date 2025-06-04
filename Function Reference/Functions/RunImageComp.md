# RunImageComp

```pascal
PROCEDURE RunImageComp(
				FilePath    : STRING;
				savedView   : STRING;
				SettingsDir : STRING;
				imageWidth  : INTEGER;
				imageHeight : INTEGER);
```

```python
def vs.RunImageComp(FilePath, savedView, SettingsDir, imageWidth, imageHeight):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|FilePath|STRING|This is the file path to the test file|
|savedView|STRING|The name of the saved view test|
|SettingsDir|STRING|The path to the directory where the settings.csv file is|
|imageWidth|INTEGER|The width in pixels of the image this function will save of the saved view.  This should be close to the width of the reference image.|
|imageHeight|INTEGER|The height in pixels of the image this function will save of the saved view.  This should be close to the height of the reference image.|

## Version
Availability: from Vectorworks 2020

## Category
* [Utility](../Categories/Utility.md)
