# DBSetFormatConn

## Description
Set ODBC connection for the specified format.

```pascal
FUNCTION DBSetFormatConn(
				formatName : STRING;
				database   : STRING;
				tableName  : STRING): BOOLEAN;
```

```python
def vs.DBSetFormatConn(formatName, database, tableName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|formatName|STRING|The format name.|
|database|STRING|The name of the data source.|
|tableName|STRING|The table name.|

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
