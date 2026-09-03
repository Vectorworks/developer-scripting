# DBSetFormatFieldConn

## Description
Set ODBC connection for the specified format field.

```pascal
FUNCTION DBSetFormatFieldConn(
				formatName : STRING;
				fieldName  : STRING;
				columnName : STRING;
				linkType   : INTEGER): BOOLEAN;
```

```python
def vs.DBSetFormatFieldConn(formatName, fieldName, columnName, linkType):
    return BOOLEAN
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
resultOK := DBSetFormatFieldConn('Example', 'MyRecord', 'Example', 1);
```
```python
import vs

# Set ODBC connection for the specified format field.
formatName = 'MyRecord'
fieldName = 'MyField'
columnName = 'Example'
linkType = 0

ok = vs.DBSetFormatFieldConn(formatName, fieldName, columnName, linkType)
if ok:
    vs.Message('DBSetFormatFieldConn succeeded')
else:
    vs.Message('DBSetFormatFieldConn failed')
```

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
