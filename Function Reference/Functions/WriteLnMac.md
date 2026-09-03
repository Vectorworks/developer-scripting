# WriteLnMac

## Description
Writes a line of data to a text file using Macintosh character encoding for extended ASCII characters (128-255). This allows extended character data to be properly read and displayed by VectorWorks on Windows systems (VectorWorks by default uses Macintosh encoding for extended character values).

The line of data written to file is terminated with a return character combination appropriate for the platform on which the file is being written.

```pascal
PROCEDURE WriteLnMac(z : ANY);
```

```python
def vs.WriteLnMac(z):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|z|ANY|   |

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
CONST
Vendor = 'ACME';
Price = 123.45;
Tax = 1.07;
BEGIN
Open('Output.txt');
WriteLnMac('Mfr/Cost: ', Vendor, '/', Price + Tax);
Close('Output.txt');
END;
RUN(Example);
```
#### Python ####
```python

```

```pascal
BEGIN
	wLineCount:=1;
	IF kDebugMode THEN WriteLn('WriteTable to file rewriting : ', fullpath);
	Rewrite(fullpath);
	WriteLnMac(gNumLinesData);

GetChoiceCount(dialogID, 4, itemCount);
for cnt := 0 to itemCount - 1 do BEGIN
	GetChoiceText(dialogID, 4, cnt, temp_s);
	WriteLnMac(temp_s);
	stringCnt := stringCnt + 1;
	strings[stringCnt] := temp_s;
END;

BEGIN
	IF OpenAbsError(prefPath, GetLocStr(12000, 3), False, fullName) = 0 THEN BEGIN
		Close(fullName);
		ReWrite(fullName);
		WriteLnMac(finishCnt);
		for cnt := 1 to finishCnt do BEGIN
			IF finishes[cnt].des = '' THEN finishes[cnt].des := '-';
			WriteLnMac('-', Chr(9), '-', Chr(9), finishes[cnt].loc, Chr(9), finishes[cnt].key, Chr(9), finishes[cnt].des);
		END;
```
```python
vs.WriteLnMac(0)
```

## See Also
VS Functions:
[WriteLn](WriteLn.md)

## Version
Availability: from VectorWorks9.0

## Category
* [File I@O](../Categories/File%20IO.md)
