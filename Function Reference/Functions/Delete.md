# Delete

## Description
Procedure Delete removes a substring from the specified source string.

```pascal
PROCEDURE Delete(
				VAR source : DYNARRAY[] of CHAR;
				index      : INTEGER;
				count      : INTEGER);
```

```python
def vs.Delete(source, index, count):
    return source
```

## Parameters
|Name|Type|Description|
|---|---|---|
|source|DYNARRAY[] of CHAR|Source string.|
|index|INTEGER|Start position in text string.|
|count|INTEGER|Length of substring.|

## Remarks
Per Raymond Mullin, on the VS list, there is a bug in Delete that prevents it from getting the last character if the string is a dynarray of char. The following test script should leave T = '', but it leaves T = '7'.

<code lang="pas">
PROCEDURE DeleteTest;
VAR
T :DYNARRAY [] of CHAR;
BEGIN
T := '1234567';
Delete(T, 1, 7);
Message('T: ', T);
END;
RUN(DeleteTest);
</code>

## Examples
#### VectorScript ####
```pascal
theStr:='A sample string';
Delete(theStr,3,7);
{deletes 'sample' from the string value}
```
#### Python ####
```python
def DeleteTest():
	T = '1234567'
	T = vs.Delete(T, 1, 7)
	vs.Message('T: ', T)

DeleteTest()
```

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
