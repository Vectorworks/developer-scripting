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
#### VectorScript ####
```pascal
BEGIN
  Open('MyData');
  WHILE NOT EOLN('MyData') DO BEGIN
    Read(a,b,c,d);
  END;

  Close('MyData');
END;
```
#### Python ####
```python

```

```pascal
BEGIN
For L1 := 1 to (NumRecFields) DO
	IF NOT EOLN(LoadFile) THEN Read(gChosenFields[L1]);
NumSelected := 0;
{Now we need to load the linking into the dialog fields}
For L2 := 1 to (NumRecFields) DO {Load all but the unique ID Field into the dialog}
	BEGIN

BEGIN
   	NumOfFields := 0;
   	Open(TheFile);
   	While Not EOLN(TheFile) DO
	{Fix this procedure so that it works correctly and actually loads in empty fields correctly
		Currently the read command does NOT treat consecutive delimeters correctly}
   		BEGIN
			NumOfFields := NumOfFields + 1;
			Read(TmpString);
			IncomingFieldNames[NumOfFields] := TmpString;
    	END;
```
```python
result = vs.EOLN('file.txt')
```

## Version
Availability: from All Versions

## Category
* [File I@O](../Categories/File%20IO.md)
