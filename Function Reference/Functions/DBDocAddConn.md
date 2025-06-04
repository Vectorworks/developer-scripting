# DBDocAddConn

## Description
Add a database connection to the current document

```pascal
FUNCTION DBDocAddConn(
				dsn      : DYNARRAY[] of CHAR;
				userName : DYNARRAY[] of CHAR;
				password : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.DBDocAddConn(dsn, userName, password):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dsn|DYNARRAY[] of CHAR|Data source name.|
|userName|DYNARRAY[] of CHAR|Username. Pass empty string if not applicable.|
|password|DYNARRAY[] of CHAR|Password. Pass empty string if not applicable.|

## Remarks
If a SQLite file does not exist at the specified location then a new database file will be created. { from Vectorworks 2014 }

## Examples
==== VectorScript ====
```pascal
{ODBC connection needs DSN name}
PROCEDURE ConnectionSample;
VAR
	Tables : DYNARRAY [] OF CHAR;
	User : DYNARRAY [] OF CHAR;
	Pass : DYNARRAY [] OF CHAR;
	res : BOOLEAN;
BEGIN
	User := 'root';
	Pass := 'rootpass';
	res := DBDocAddConn( 'MyTestODBCDatabase', User, Pass );
	res := DBDocGetTables( 'MyTestODBCDatabase', Tables );
	AlrtDialog( concat( 'Result = ', res, ' ', Tables ) );
END;
RUN( ConnectionSample );

{ SQLite connection is available from VW 2014 }
{ SQLite connection needs [sqlite] prefix and full path to the database file }
PROCEDURE SQLiteConnTest;
VAR
        Tables : DYNARRAY [] OF CHAR;
	res : BOOLEAN;
BEGIN
	res := DBDocAddConn( '[sqlite]C:SQLiteSamplesMytestSQLite.sqlite', '', '' );
	res := DBDocGetTables( '[sqlite]C:SQLiteSamplesMytestSQLite.sqlite', Tables );
	AlrtDialog( Tables );
END;
RUN( SQLiteConnTest );
```
==== Python ====
```python
#{ SQLite connection is available from VW 2014 }
#{ SQLite connection needs [sqlite] prefix and full path to the database file }
def SQLiteConnTest():
	res = vs.DBDocAddConn( '[sqlite]C:SQLiteSamplesMytestSQLite.sqlite', '', '' );
	res, Tables = vs.DBDocGetTables( '[sqlite]C:SQLiteSamplesMytestSQLite.sqlite' )
	vs.AlrtDialog( Tables );
SQLiteConnTest()
```

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
