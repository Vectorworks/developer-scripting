# DBDocGetDB

## Description
Returns a string representing a ';' delimited list of the databases currently connected to the document.

```pascal
FUNCTION DBDocGetDB(VAR outDatabases : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.DBDocGetDB():
    return (BOOLEAN, outDatabases)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outDatabases|DYNARRAY[] of CHAR|   |

## Remarks
*_c_* 2010.09.27: Some observations:
* no database connections in the document: returns FALSE
* one database connected to the document: the string won't end with colon ";".
* more databases connected: colon-separated string of database names.

## Examples
#### VectorScript ####
```pascal
PROCEDURE ODBCtest;
    VAR
        outDatabases : DYNARRAY [] OF CHAR;
BEGIN
    outDatabases := '';	
    IF DBDocGetDB(outDatabases) THEN BEGIN
        AlrtDialog(outDatabases); { colon-separated list of databases, if more than one }
        { .... }
    END;
END;
Run(ODBCtest);
```
#### Python ####
```python
def ODBCtest():
	outDatabases = ''	
	hasDB,  outDatabases= vs.DBDocGetDB()
	if hasDB:
		vs.AlrtDialog(outDatabases); #{ colon-separated list of databases, if more than one }
ODBCtest()
```

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
