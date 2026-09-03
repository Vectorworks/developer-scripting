# Concat

## Description
Function Concat combines, or concatenates, all the specified parameters in order and returns the resultant string.

```pascal
FUNCTION Concat(txt : DYNARRAY[] of CHAR): DYNARRAY[] of CHAR;
```

```python
def vs.Concat(txt):
    return DYNARRAY[] of CHAR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|txt|DYNARRAY[] of CHAR|   |

## Remarks
*\_c\_*, 2015.05.23: You can use [Concat](Concat.md) to convert numbers to strings, but it uses exclusively a dot "." as symbol for the decimal marker, it outputs the number as seen from inside VS. See the table below for a list of routines formatting according to your system's settings.

**Decimal marker symbol usage**

| Metric: ',' Example | American '.' Example |
|---------------------|---------------------|
| 100,123             | 100.123             |

| Formatting routines | Non formatting routines |
|---------------------|------------------------|
| [Num2Str](Num2Str.md), [Num2StrF](Num2StrF.md), [Angle2Str](Angle2Str.md), [Area2Str](Area2Str.md), [Volume2Str](Volume2Str.md)<br>`Num2Str(3, 100.123) { --> 100,123 on metric systems }`<br>`Num2Str(3, 100.123) { --> 100.123 on American systems }` | [Concat](Concat.md)<br>`Concat(100.123) { --> 100.123 on any system }` |

## Examples
#### VectorScript ####
```pascal
AlrtDialog(Concat('A', 'sample', 'string'));
```
#### Python ####
```python
vs.AlrtDialog(vs.Concat('A', 'sample', 'string'))
```

```pascal
ELSE BEGIN
	dataFile := Concat (folderPath, kFileName);
	sizeNotFound := TRUE;
	Open (datafile);
	ReadLn (dataUPI);

theLabel := Concat(GetPlugInString(3004), Chr(13), Chr(13),
					GetPlugInString(3006), Num2Str(2, theta), Chr(13),
					GetPlugInString(3007), Num2StrF(D), Chr(13),
					GetPlugInString(3008), Num2StrF(T), Chr(13),
					GetPlugInString(3009), Num2StrF(L), Chr(13),
					GetPlugInString(3010), Num2StrF(theRadius));

ELSE BEGIN
	IF gNumSymbols = 1 THEN tempStr1 := GetPlugInString (3018)
	ELSE tempStr1 := GetPlugInString (3019);
	tempStr2 := Concat (GetPlugInString (3016), gRecordName, GetPlugInString (3017), Num2Str (0, gNumSymbols), tempStr1);
	AlrtDialog (tempStr2);
END;
```
```python
if dMmarkerSize <= 0:
	dMmarkerSize = 1 * dUPI
	vs.PMarker_Size = dMmarkerSize
	vs.SetRField( gObjHandle, gObjName, 'Marker Size', vs.Concat( dMmarkerSize) )
	recordFormatHandle = vs.GetObject(gObjName)
	vs.SetRField( recordFormatHandle, gObjName, 'Marker Size', vs.Concat( dMmarkerSize) )
```

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
