# StdReadLn

## Description
Procedure StdReadLn will read data from a currently open text file. The variable length parameter list returns the read data in the specified parameters.

Supported data types include INTEGER, REAL, LONGINT, CHAR or STRING. Non STRING data values must be separated by a tab or space to be correctly read into variables. If the procedure encounters an EOF(end-of-file) marker, an error is generated. StdReadLn positions the file position pointer to the beginning of a new line after the procedure is called.

StdReadLn reads data according to the Pascal language standard. This differs from the [ReadLn](ReadLn.md) procedure found in VectorScript primarily when reading STRING data. StdReadLn will read all characters, including tabs and spaces, as a single string value. [ReadLn](ReadLn.md) will detect tabs as delimiters, allowing multiple string values to be assigned to variables. Additionally, [ReadLn](ReadLn.md) will read UTF-8 encoded files.

```pascal
PROCEDURE StdReadLn(VAR z : ANY);
```

```python
def vs.StdReadLn():
    return z
```

## Parameters
|Name|Type|Description|
|---|---|---|
|z|ANY|   |

## Examples
#### VectorScript ####
```pascal
GetFile(fName);
IF NOT DidCancel THEN BEGIN
Open(fName);
StdReadLn(partID,partName);
END;
```
#### Python ####
```python

```

```pascal
BEGIN
	{Dialog supports CR which ReadLn sees as a delimiter so must parse the line}
	TempLongString := '';
	StdReadLn(TempLongString);
	ParseLongString(TempLongString,kTab,MasterDataTable [n,1]);{VW Sheet Name with no suffix} {SheetType}
	ParseLongString(TempLongString,kTab,MasterDataTable [n,2]);{Layer Name with no suffix} {LayerType}
	ParseLongString(TempLongString,kTab,MasterDataTable [n,3]);{Class Name}
	ParseLongString(TempLongString,kTab,MasterDataTable [n,4]);{Layer Option Index} {always 5}

fileOK := FALSE;
Open(fullName);
IF GetLastFileErr = 0 THEN BEGIN
	for cnt := 1 to numHeadRows DO StdReadLn(dynaChar); {Get rid OF the header rows.}
	inCnt := 0;
	fileOK := TRUE;
	while not EOF(fullName) do BEGIN
		inCnt := inCnt + 1;

if OpenRelError(GetLocStr(11112, 1), 'Lumber Sizes.txt', true, fullName) = 0 THEN BEGIN {$INCLOOD VW_Arch\Data\Lumber Sizes.txt}
	nom_cnt := 0;
	keepGoing := TRUE;
	while keepGoing do BEGIN
		StdReadLn(temp1_s);
		if (Pos('Imperial', temp1_s) = 1) | (Pos('Metric', temp1_s) = 1) then StoreNominals(temp1_s) ELSE
		if (Pos('Minimum length (Imperial):',    temp1_s) = 1) then StoreLenMinInc(temp1_s, minLenImp) ELSE
		if (Pos('Minimum length (Metric):',      temp1_s) = 1) then StoreLenMinInc(temp1_s, minLenMet) ELSE
		if (Pos('Length increments (Imperial):', temp1_s) = 1) then StoreLenMinInc(temp1_s, lenIncImp) ELSE
```
```python
result = vs.StdReadLn()
```

## Version
Availability: from VectorWorks8.0

## Category
* [File I@O](../Categories/File%20IO.md)
