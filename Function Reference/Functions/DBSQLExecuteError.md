# DBSQLExecuteError

## Description
Return information about the last error occured in the ODBC API functions.

```pascal
FUNCTION DBSQLExecuteError(
				VAR message      : DYNARRAY[] of CHAR;
				VAR state        : DYNARRAY[] of CHAR;
				VAR code         : LONGINT;
				VAR internalDesc : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.DBSQLExecuteError():
    return (BOOLEAN, message, state, code, internalDesc)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|DYNARRAY[] of CHAR|This is the message text.|
|state|DYNARRAY[] of CHAR|The state provides detailed information about the cause of a warning or error.|
|code|LONGINT|This is the native error number.|
|internalDesc|DYNARRAY[] of CHAR|It is not in use.|

## Remarks
The '''message text''' is the text of the diagnostic.

The '''state''' is a five character SQLSTATE code. The first two characters indicate the class and the next three indicate the subclass. SQLSTATEs provide detailed information about the cause of a warning or error. For a complete list of states see [http://msdn.microsoft.com/en-us/library/ms714687%28v=vs.85%29.aspx Appendix A: ODBC Error Codes]. A list of ODBC 2.x to ODBC 3.x SQLSTATE mappings can be found [http://msdn.microsoft.com/en-us/library/ms712451.aspx here].

The '''native error code''' is a code specific to the data source. This number is often extremely useful to the driver developers in locating an internal error or state. If you are reporting a bug for which you obtained an error you should always quote the ODBC function called, the error text and this native number.

Example of ODBC error reported by Vectorwroks and occured in FileMaker driver:
''[65535] Driver error: 08S01
[FileMaker][FileMaker] Failed to connect to listener (2)''

'''NB! However, there is no guarantee that all drivers return them.'''

## Examples
==== VectorScript ====
```pascal
PROCEDURE Test;
VAR
	ok : BOOLEAN;
	message, state, internalDesc : DYNARRAY[] OF CHAR;
	code, colCnt, resSetInst : LONGINT;
begin
	ok := DBDocAddConn( 'MyTestODBCDatabase', '', '' );
	ok := DBSQLExecuteDSN( 'MyTestODBCDatabase', '', '', 'SELECT * FROM Spaces', colCnt, resSetInst );
	if not ok then
	begin
		ok := DBSQLExecuteError(message, state, code, internalDesc);
		AlrtDialog(Concat('state: ', state, Chr(13), 'message: ', message, Chr(13), 'code: ', code, Chr(13), 'intDesc: ', internalDesc));
	end;
end;

RUN(Test);
```
==== Python ====
```python
import vs
ok = vs.DBDocAddConn( 'MyTestODBCDatabase', '', '' )
colCnt = 0
resSetInst = 0
ok = vs.DBSQLExecuteDSN( 'MyTestODBCDatabase', '', '', 'SELECT * FROM Spaces', colCnt, resSetInst )
ok, message, state, code, internalDesc = vs.DBSQLExecuteError()
vs.AlrtDialog('state: ' + state + '\nmessage: ' + message + '\ncode: ' + str(code) + '\nintDesc: ' + internalDesc)
```

## Version
Availability: from Vectorworks 2012

## Category
* [ODBC](../Categories/ODBC.md)
