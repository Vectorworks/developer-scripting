# UprString

## Description
Procedure UprString converts all characters in the specified string to upper case.

```pascal
PROCEDURE UprString(VAR str : DYNARRAY[] of CHAR);
```

```python
def vs.UprString(str):
    return str
```

## Parameters
|Name|Type|Description|
|---|---|---|
|str|DYNARRAY[] of CHAR|Source string.|

## Examples
==== VectorScript ====
```pascal
revisedString := 'vectorworks';
UprString(revisedString);
{Sets revisedString equal to 'VECTORWORKS'}
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
