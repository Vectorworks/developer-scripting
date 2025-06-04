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

## Version
Availability: from Vectorworks 2018

## Category
* [Special - QuickTime](../Categories/Special%20-%20QuickTime.md)
