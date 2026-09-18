# QTGetMovieOptionsN

```pascal
PROCEDURE QTGetMovieOptionsN(
				movieRef         : INTEGER;
				VAR frameRate    : REAL;
				VAR keyFrameRate : LONGINT;
				VAR frameWidth   : LONGINT;
				VAR frameHeight  : LONGINT);
```

```python
def vs.QTGetMovieOptionsN(movieRef):
    return (frameRate, keyFrameRate, frameWidth, frameHeight)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|movieRef|INTEGER|Index of QuickTime movie stream.|
|frameRate|REAL|Frame rate of movie|
|keyFrameRate|LONGINT|keyFrameRate|
|frameWidth|LONGINT|Frame width of the movie stream.|
|frameHeight|LONGINT|Frame height of the movie stream.|

## Examples
```pascal
BEGIN
	QTGetMovieOptionsN(QTMovieID, QTFrameRate, QTKeyFrameRate, QTFrameWidth, QTFrameHeight);
	If Not UserSetQTOptions then QTSetMovieOptionsN(QTMovieID, 15, 30, FALSE, FALSE, QTFrameWidth, QTFrameHeight);
	QTMovieID := QTOpenMovieFileN(QTMovieID, QTFileName, QTFrameWidth, QTFrameHeight);
			CreateSceneAnimation; {this Does everyting we need. figures out how long the movie is etc.}
	RestoreSavedStatus;
```
```python
import vs

movieRef = 1

frameRate, keyFrameRate, frameWidth, frameHeight = vs.QTGetMovieOptionsN(movieRef)
vs.Message('QTGetMovieOptionsN returned: ' + str((frameRate, keyFrameRate, frameWidth, frameHeight)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Special - QuickTime](../Categories/Special%20-%20QuickTime.md)
