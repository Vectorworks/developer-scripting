## VectorScript

```pascal
PROCEDURE Test;
VAR
	res : BOOLEAN;
	colCnt, resSetInst, colIndex, rowIndex : LONGINT;
	colName, colValue : DYNARRAY [] OF CHAR;
BEGIN
	res := DBSQLExecuteDSN( 'My Building', '', '', 'SELECT * FROM Spaces', colCnt, resSetInst );
	AlrtDialog( Concat( 'Execute: res=', res, ' colCnt=', colCnt, ' resSetInst=', resSetInst ) );

	rowIndex := 1;
	REPEAT
		FOR colIndex := 1 TO colCnt DO BEGIN
			res := DBSQLExecuteGet( resSetInst, colIndex, colName, colValue );

			AlrtDialog( Concat( 'Result: row=', rowIndex, ' col=', colIndex, ' colName=', colName, ' colValue=', colValue ) );
		END;

		rowIndex  := rowIndex  + 1;
	UNTIL NOT DBSQLExecuteNext( resSetInst );

	DBSQLExecuteDelete( resSetInst );
END;
RUN(Test);
```

## Python

```python
def Test():
	res, colCnt, resSetInst = vs.DBSQLExecuteDSN( 'My Building', '', '', 'SELECT * FROM Spaces' )
	vs.AlrtDialog( vs.Concat( 'Execute: res=', res, ' colCnt=', colCnt, ' resSetInst=', resSetInst ) )
	
	rowIndex = 1
	dbNext = True
	while dbNext:
		for colIndex in range(1, colCnt):
			res, colName, colValue = vs.DBSQLExecuteGet( resSetInst, colIndex )
			vs.AlrtDialog( Concat( 'Result: row=', rowIndex, ' col=', colIndex, ' colName=', colName, ' colValue=', colValue ) )

		rowIndex  = rowIndex  + 1
		dbNext = vs.DBSQLExecuteNext( resSetInst )

	vs.DBSQLExecuteDelete( resSetInst )

Test()
```
