# QTCloseMovieFile

## Description
Closes the specified QuickTime movie file.

```pascal
PROCEDURE QTCloseMovieFile(movieRef : INTEGER);
```

```python
def vs.QTCloseMovieFile(movieRef):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|movieRef|INTEGER|Index of QuickTime movie stream.|

## Examples
```pascal
			IF gShowFrameCounter THEN SetupFrameCounter;
			GetSunrise(gSunriseHour, gSunriseMinute, gDoQTFrames);
			GoTilSunset(gSunriseHour, gSunriseMinute, gSunSetHour, gSunSetMinute, gDoQTFrames);
		END;
	QTCloseMovieFile(gMovieRef);
END
```
```python
import vs

# Closes the specified QuickTime movie file.
movieRef = 1

vs.QTCloseMovieFile(movieRef)
```

## Version
Availability: from VectorWorks8.5

## Category
* [Special - QuickTime](../Categories/Special%20-%20QuickTime.md)
