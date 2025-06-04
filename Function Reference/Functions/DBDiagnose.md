# DBDiagnose

## Description
Tests ODBC connectivity and creates log file in application folder. Returns true if succeeded.

First it opens a dialog "Database Connection" dialog. Choose a data source from the popup.

```pascal
FUNCTION DBDiagnose : BOOLEAN;
```

```python
def vs.DBDiagnose():
    return BOOLEAN
```

## Examples
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	isOK : BOOLEAN;
BEGIN
	isOK := DBDiagnose;
END;

Run(Test);
```
#### Python ####
```python
import vs
def Test():
	vs.DBDiagnose()

Test()
```

## Version
Availability: from Vectorworks 2015

## Category
* [ODBC](../Categories/ODBC.md)
