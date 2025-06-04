# DBObjSQLGetRead

## Description
Get an object's SQL query for ODBC read.

```pascal
FUNCTION DBObjSQLGetRead(
				hRecord         : HANDLE;
				VAR SQLSentence : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.DBObjSQLGetRead(hRecord):
    return (BOOLEAN, SQLSentence)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hRecord|HANDLE|   |
|SQLSentence|DYNARRAY[] of CHAR|   |

## Examples
==== VectorScript ====
```pascal
PROCEDURE Test;
VAR
	recordName, query : DYNARRAY [] OF CHAR;
	hCurrentLayer, hCurrentObject, hRecord : HANDLE;
	i, cnt : LONGINT;
	res : BOOLEAN;

BEGIN
	hRecord := NIL;
	{Select only objects with record attached}
	recordName := 'TestRecord';
	DSelectAll;
	SelectObj(INSYMBOL & INVIEWPORT & (R IN [recordName ]));

	{Get quesries of selected object}
	hCurrentLayer := FLayer; { first layer }
	while (hCurrentLayer <> NIL) do { loop through all the layers }
	begin
		hCurrentObject := FSObject(hCurrentLayer); { first selected object in layer }
		while hCurrentObject <> NIL do { loop through all the objects }
		begin
			{find the record}
			cnt := NumRecords(hCurrentObject );
			for i := 1 to cnt do 
			begin
				hRecord := GetRecord(hCurrentObject , i);
				if hRecord <> NIL then begin
					if GetName(hRecord) = recordName then begin
						res := DBObjSQLGetRead(hRecord, query); 
						AlrtDialog(query);
					end;
				end;
			end;
			hCurrentObject := NextSObj(hCurrentObject); { next selected object }
		end;
		hCurrentLayer := NextLayer(hCurrentLayer); { next layer }
	end;
	
END;
RUN(Test);
```
==== Python ====
```python
import vs

def Test():
	hRecord = vs.Handle()
	#Select only objects with record attached
	recordName = 'TestRecord'
	vs.DSelectAll()
	vs.SelectObj("INSYMBOL & INVIEWPORT & (R IN ['" + recordName + "'])" )

	#Get quesries of selected object
	hCurrentLayer = vs.FLayer() #First Layer
	while hCurrentLayer != vs.Handle(): #loot through layers

		hCurrentObject = vs.FSObject(hCurrentLayer) #first selected object
		while hCurrentObject != vs.Handle(): #loop through all the objects

			#find the object
			cnt = vs.NumRecords(hCurrentObject)
			for i in range(0,cnt):

				hRecord = vs.GetRecord(hCurrentObject, i + 1)
				if hRecord != vs.Handle():
					if vs.GetName(hRecord) == recordName:
						res, query = vs.DBObjSQLGetRead(hRecord)
						vs.AlrtDialog(query)

			hCurrentObject = vs.NextSObj(hCurrentObject)
		
		hCurrentLayer = vs.NextLayer(hCurrentLayer)


Test()
```

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
