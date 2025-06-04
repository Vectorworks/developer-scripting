# Insert

## Description
Procedure Insert will insert the specified string into a destination string.

```pascal
PROCEDURE Insert(
				source   : DYNARRAY[] of CHAR;
				VAR dest : DYNARRAY[] of CHAR;
				index    : INTEGER);
```

```python
def vs.Insert(source, index):
    return dest
```

## Parameters
|Name|Type|Description|
|---|---|---|
|source|DYNARRAY[] of CHAR|String to be inserted.|
|dest|DYNARRAY[] of CHAR|Destination string.|
|index|INTEGER|Position where string is to be inserted.|

## Examples
#### VectorScript ####
```pascal
theStr:='sample';
originalStr:='A string';
Insert(theStr,originalStr,3);
{inserts 'sample' into the target string}
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
