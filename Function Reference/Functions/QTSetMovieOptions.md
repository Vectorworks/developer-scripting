# QTSetMovieOptions

## Description
Sets the QuickTime movie frame rate and key frame rate for the referenced movie stream. The standard QuickTime compression options dialog can also be optionally displayed.

```pascal
PROCEDURE QTSetMovieOptions(
				movieRef      : INTEGER;
				frameRate     : REAL;
				keyFrameRate  : LONGINT;
				useDlg        : BOOLEAN;
				useDlgPreview : BOOLEAN);
```

```python
def vs.QTSetMovieOptions(movieRef, frameRate, keyFrameRate, useDlg, useDlgPreview):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|movieRef|INTEGER|Index of QuickTime movie stream.|
|frameRate|REAL|Frame rate of movie.|
|keyFrameRate|LONGINT|Key frame rate of movie.|
|useDlg|BOOLEAN|Display QuickTime comprssion options dialog.|
|useDlgPreview|BOOLEAN|Show dialog preview.|

## Examples
```pascal
BEGIN
	QTSetMovieOptions(gMovieRef, 15, 5, True, FALSE);
	IF NOT(DidCancel) THEN
		BEGIN
			gLightHan := CreateLight(1,1,1,0, TRUE,TRUE);
			IF gShowFrameCounter THEN SetupFrameCounter;
```
```python
import vs

# Sets the QuickTime movie frame rate and key frame rate for the referenced
# movie stream.
movieRef = 1
frameRate = 1.0
keyFrameRate = 2
useDlg = True
useDlgPreview = True

vs.QTSetMovieOptions(movieRef, frameRate, keyFrameRate, useDlg, useDlgPreview)
```

## Version
Availability: from VectorWorks8.5

## Category
* [Special - QuickTime](../Categories/Special%20-%20QuickTime.md)
