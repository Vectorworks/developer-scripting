# QTWriteFrame

## Description
Captures the active document window and writes a frame to the specified QuickTime movie file.

```pascal
PROCEDURE QTWriteFrame(movieRef : INTEGER);
```

```python
def vs.QTWriteFrame(movieRef):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|movieRef|INTEGER|Index of QuickTime movie stream.|

## Remarks
This function will likely also draw to the screen as a pseudo-progress indicator.

## Examples
```pascal
		IF fMinute < 10 THEN fDisplayStr := Concat(fDisplayStr, '0');
		fDisplayStr := Concat(fDisplayStr, Num2Str(0, fMinute));
		SetText(gFrameCounterHan, fDisplayStr);
	END;
	QTWriteFrame(gMovieRef);
END;

	ProgressDlgYield( 1 );
	ProgressDlgSetMeter( Concat( kProcFrame, Num2Str( 0, CurrentFrame ), kOfNumber, Num2Str( 0, TotNumFrames ) ) );
	CurrentFrame := CurrentFrame + 1;
	OutputLights;
	IF NOT kNoQTOut THEN QTWriteFrame(QTMovieID);
END;
```
```python
import vs

# Captures the active document window and writes a frame to the specified
# QuickTime movie file.
movieRef = 1

vs.QTWriteFrame(movieRef)
```

## Version
Availability: from VectorWorks8.5

## Category
* [Special - QuickTime](../Categories/Special%20-%20QuickTime.md)
