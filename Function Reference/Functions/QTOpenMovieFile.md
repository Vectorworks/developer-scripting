# QTOpenMovieFile

## Description
Creates or opens a QuickTime movie file for writing.

```pascal
FUNCTION QTOpenMovieFile(fileName : STRING): INTEGER;
```

```python
def vs.QTOpenMovieFile(fileName):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fileName|STRING|Name of movie file.|

## Examples
```pascal
BEGIN
	gMovieRef := QTOpenMovieFile(gFileName);;
	IF (gMovieRef <> -1) THEN
		BEGIN
			QTSetMovieOptions(gMovieRef, 15, 5, True, FALSE);
			IF NOT(DidCancel) THEN
```
```python
import vs

# Creates or opens a QuickTime movie file for writing.
fileName = 'C:/Temp/example.txt'

resultN = vs.QTOpenMovieFile(fileName)
vs.Message('QTOpenMovieFile returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks8.5

## Category
* [Special - QuickTime](../Categories/Special%20-%20QuickTime.md)
