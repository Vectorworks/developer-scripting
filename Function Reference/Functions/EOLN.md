# EOLN

## Description
Function EOLN returns TRUE if the file pointer of an open text file has reached a carriage return within the file. Parameter fileName specifies a text file which is open for reading or writing.

```pascal
FUNCTION EOLN(fileName : STRING): BOOLEAN;
```

```python
def vs.EOLN(fileName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fileName|STRING|Name of file.|

## Examples
==== VectorScript ====
```pascal
BEGIN
  Open('MyData');
  WHILE NOT EOLN('MyData') DO BEGIN
    Read(a,b,c,d);
  END;

  Close('MyData');
END;
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [File I@O](../Categories/File%20IO.md)
