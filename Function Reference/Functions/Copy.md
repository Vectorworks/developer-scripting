# Copy

## Description
Function Copy returns a substring from a specified source string.

```pascal
FUNCTION Copy(
				source : DYNARRAY[] of CHAR;
				index  : INTEGER;
				count  : INTEGER): DYNARRAY[] of CHAR;
```

```python
def vs.Copy(source, index, count):
    return DYNARRAY[] of CHAR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|source|DYNARRAY[] of CHAR|Source string.|
|index|INTEGER|Start position in text string.|
|count|INTEGER|Length of substring.|

## Examples
#### VectorScript ####
```pascal
Message(Copy('A sample string',10,6))
{returns 'string'}
```
#### Python ####
```python
vs.Message(vs.Copy('A sample string',10,6))
```

```pascal
{Azimuth or Bearing, Decimal or DMS}
IF NOT ok THEN if ValidAngStr(inBearingStr, outBearing) then BEGIN
	ok := TRUE;
	{Azimuth-DMS}
	IF ValidNumStr(Copy(inBearingStr, 1, 1), num) THEN outBearing := Compass2Cad(outBearing);
END;

BEGIN
	IF (copy(date(2,2),2,1)=':')
	THEN BEGIN
		hr:=str2num(copy(date(2,2),1,1));
		min:=str2num(copy(date(2,2),3,2));
		END

BEGIN
	recName := Copy( GetName( recordH ), 1, 5 );
	if  recName <> '__NNA'  THEN
	BEGIN
		j := j + 1;
		ALLOCATE gRecordH [1..j];
```
```python
if ( recHand != 0 ) and ( wksHand != 0 ):
	# * Get the user standard index *
	userIndex = vs.Str2Num( vs.Copy( vs.GetRField( recHand, recName, getLocStr( 12018, 2 ) ), 1, 1 ) )
	rows, cols = vs.GetWSRowColumnCount( wksHand )
	i = 1
	numClasses = rows - 1
	while (i <= numClasses ):
```

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
