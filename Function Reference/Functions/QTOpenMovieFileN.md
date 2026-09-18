# QTOpenMovieFileN

```pascal
FUNCTION QTOpenMovieFileN(
				movieRef    : INTEGER;
				fileName    : STRING;
				frameWidth  : LONGINT;
				frameHeight : LONGINT): INTEGER;
```

```python
def vs.QTOpenMovieFileN(movieRef, fileName, frameWidth, frameHeight):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|movieRef|INTEGER|MovieRefID that was already created with QTCreateMovieRefID.|
|fileName|STRING|Name of movie file.|
|frameWidth|LONGINT|Frame width of the movie file.|
|frameHeight|LONGINT|Frame height of the movie file.|

## Examples
```pascal
BEGIN
	QTGetMovieOptionsN(QTMovieID, QTFrameRate, QTKeyFrameRate, QTFrameWidth, QTFrameHeight);
	If Not UserSetQTOptions then QTSetMovieOptionsN(QTMovieID, 15, 30, FALSE, FALSE, QTFrameWidth, QTFrameHeight);
	QTMovieID := QTOpenMovieFileN(QTMovieID, QTFileName, QTFrameWidth, QTFrameHeight);
			CreateSceneAnimation; {this Does everyting we need. figures out how long the movie is etc.}
	RestoreSavedStatus;
	ResetLightingDevices;
	CleanUpMissingLight;
```
```python
import vs

movieRef = 1
fileName = 'C:/Temp/example.txt'
frameWidth = 2
frameHeight = 3

resultN = vs.QTOpenMovieFileN(movieRef, fileName, frameWidth, frameHeight)
vs.Message('QTOpenMovieFileN returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Special - QuickTime](../Categories/Special%20-%20QuickTime.md)
