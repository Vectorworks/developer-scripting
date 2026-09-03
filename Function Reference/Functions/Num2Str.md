# Num2Str

## Description
Function Num2Str converts a REAL value to a string and returns the value.

Parameter decPlace has a range of -1 to 9; if -1 is specified, the value will be returned in scientific notation.

```pascal
FUNCTION Num2Str(
				decPlace : INTEGER;
				v        : REAL): STRING;
```

```python
def vs.Num2Str(decPlace, v):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|decPlace|INTEGER|Number of decimal places.|
|v|REAL|Numeric value.|

## Remarks
*\_c\_*, 2015.05.23: You can also use [Concat](Concat.md) to convert numbers to strings, but it uses exclusively a dot "." as symbol for the decimal marker, because it outputs the number as seen from inside VS, I suppose. See further comments on the page [Concat](Concat.md).

The parameter *decPlace* can be the following values:

| Value    | Meaning                              | Sample                                 |
|----------|--------------------------------------|----------------------------------------|
| positive | round-up the value                   | 10.56 -> 10.6 (1 decimal place)        |
| 0        | round-up the value                   | 10.56 -> 11                            |
| -1       | Use scientific notation (9 decimals) | 10.56 -> 1.056000000e+001              |
| -2       | Use scientific notation (15 decimals)| 10.56 -> 1.056000000000000e+001        |

## Examples
#### VectorScript ####
```pascal
oldnumValue := 232.5148;
newStrValue := Num2Str(3, oldnumValue);
{ --> '232.515' if your system is american }
{ --> '232,515' if your system is metric }
```
#### Python ####
```python

```

```pascal
theLabel := Concat(GetPlugInString(3004), Chr(13), Chr(13),
					GetPlugInString(3006), Num2Str(2, theta), Chr(13),
					GetPlugInString(3007), Num2StrF(D), Chr(13),
					GetPlugInString(3008), Num2StrF(T), Chr(13),
					GetPlugInString(3009), Num2StrF(L), Chr(13),
					GetPlugInString(3010), Num2StrF(theRadius));

REPEAT
	alpha := alpha + 1 / incr;
	theta := Deg2Rad (alpha);
	m := (Sin (theta / 2) / theta) - (c / (2 * s));
	m := Str2Num (Num2Str (accuracy, m));
	IF m = 0 THEN
		a := alpha2

BEGIN
	IF numPlaces > 9 THEN numPlaces := 9;
	rRound := Str2Num (Num2Str (numPlaces, a));
END;
```
```python
result = vs.Num2Str(decPlace, v)
```
See also in tutorials: [10. Iterate the Drawing and Report a Summary](ai%20examples/10_IterateAndReport.md), [11. 2D Vector Math Toolkit](ai%20examples/11_VectorMathToolkit.md), [12. Polygon Area and Centroid (Shoelace Formula)](ai%20examples/12_PolygonAreaCentroid.md), [15. Uniform Arc-Length Resampling of a Polyline](ai%20examples/15_PolylineResampleUniform.md)

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
