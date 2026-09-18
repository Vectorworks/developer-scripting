# DBGetFormatFieldConn

## Description
Get ODBC connection for the specified format field.

```pascal
FUNCTION DBGetFormatFieldConn(
				formatName     : STRING;
				VAR fieldName  : STRING;
				VAR columnName : STRING;
				VAR linkType   : INTEGER): BOOLEAN;
```

```python
def vs.DBGetFormatFieldConn(formatName):
    return (BOOLEAN, fieldName, columnName, linkType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|formatName|STRING|   |
|fieldName|STRING|   |
|columnName|STRING|   |
|linkType|INTEGER|0 = Read/Write; 1 = Read Only; 2 = Write Only|

## Examples
```pascal
resultOK := DBGetFormatFieldConn('Example', 'MyRecord', 'Example', 1);
```
```python
import vs

# Get ODBC connection for the specified format field.
formatName = 'MyRecord'

ok, fieldName, columnName, linkType = vs.DBGetFormatFieldConn(formatName)
vs.Message('DBGetFormatFieldConn returned: ' + str((ok, fieldName, columnName, linkType)))
```

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
