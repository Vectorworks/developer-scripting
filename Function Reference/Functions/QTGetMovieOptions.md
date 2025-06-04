# QTGetMovieOptions

## Description
Retrieves the QuickTime movie frame rate and key frame rate for the referenced movie stream.

```pascal
PROCEDURE QTGetMovieOptions(
				movieRef         : INTEGER;
				VAR frameRate    : REAL;
				VAR keyFrameRate : LONGINT);
```

```python
def vs.QTGetMovieOptions(movieRef):
    return (frameRate, keyFrameRate)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|movieRef|INTEGER|Index of QuickTime movie stream.|
|frameRate|REAL|Frame rate of movie|
|keyFrameRate|LONGINT|Key frame rate of movie.|

## Version
Availability: from VectorWorks8.5

## Category
* [Special - QuickTime](../Categories/Special%20-%20QuickTime.md)
