# QTSetMovieOptionsN

```pascal
PROCEDURE QTSetMovieOptionsN(
				movieRef      : INTEGER;
				frameRate     : REAL;
				keyFrameRate  : LONGINT;
				useDLG        : BOOLEAN;
				useDlgPreview : BOOLEAN;
				frameWidth    : LONGINT;
				frameHeight   : LONGINT);
```

```python
def vs.QTSetMovieOptionsN(movieRef, frameRate, keyFrameRate, useDLG, useDlgPreview, frameWidth, frameHeight):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|movieRef|INTEGER|Index of QuickTime movie stream.|
|frameRate|REAL|Frame rate of movie.|
|keyFrameRate|LONGINT|Key frame rate of the movie.|
|useDLG|BOOLEAN|Display QuickTime Video Settings dialog.|
|useDlgPreview|BOOLEAN|Show dialog preview.|
|frameWidth|LONGINT|Frame width for the movie file.|
|frameHeight|LONGINT|Frame height for the movie file.|

## Examples
```pascal
				END;
		END;
	END;
30: BEGIN {QuickTime Settings...}
	QTSetMovieOptionsN(QTMovieID, 15, 30, True, FALSE, QTFrameWidth, QTFrameHeight);
	UserSetQTOptions := TRUE;
	END;
```
```python
import vs

movieRef = 1
frameRate = 1.0
keyFrameRate = 2
useDLG = True
useDlgPreview = True
frameWidth = 3
frameHeight = 10

vs.QTSetMovieOptionsN(movieRef, frameRate, keyFrameRate, useDLG, useDlgPreview, frameWidth, frameHeight)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Special - QuickTime](../Categories/Special%20-%20QuickTime.md)
