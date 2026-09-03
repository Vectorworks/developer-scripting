# EvalStr

## Description
Evaluates whether an object meets the specified search criteria. 

When used with record criteria, it will determine whether a specific record is attached to the object; if used with record-field criteria, it will return the value of the field as a STRING.

```pascal
FUNCTION EvalStr(
				h : HANDLE;
				c : CRITERIA): STRING;
```

```python
def vs.EvalStr(h, c):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle of object to which the search criteria will be applied.|
|c|CRITERIA|Search criteria.|

## Remarks
*\_c\_*, 2015.06.17: 
Don't forget the brakets or it will block the rest of the script in a totally unpredictable way upon any special char. I suppose that it tries to parse the rest of the script as criteria:
 crit := '.'; { suspiciously dangerous special char }
 str := EvalStr(gTargetH, crit); { strange failure of parts of the script after this call ! }
 str := EvalStr(gTargetH, (crit)); { correct }

## Examples
#### VectorScript ####
```pascal
dataValue:= EvalStr(handleToObject,('Part Info'.'Serial No.'));
```
#### Python ####
```python

```

```pascal
BEGIN
	CASE GetType(symH) OF
		16: BEGIN
			IF (EvalStr(symH, R IN [kLIRecName])=TrueStr) THEN BEGIN
				curRow:=InsertLBItem(dialogIDIM, kBrowser, GetNumLBItems(dialogIDIM, kBrowser), GetSDName(symH));
				symCount:=GetNumLBItems(dialogIDIM, kBrowser);
				ALLOCATE gSymInfoList[1..symCount];
				gSymInfoList[symCount].LBid:=symCount;
				gSymInfoList[symCount].han:=symH;

BEGIN
	CASE GetType(symH) OF
		16: BEGIN
			IF (EvalStr(symH, R IN [kLIRecName])=TrueStr) THEN BEGIN
				typeStr:=GetRField(symH, kLIRecName, kLIPTypeFld);
				IF typeStr='' THEN typeStr:=GetSDName(symH);
				IF (gNumInst = 0) | (NOT isInstInList(gInstList, typeStr)) THEN BEGIN
					gNumInst:=gNumInst+1;
					ALLOCATE gInstList[1..gNumInst];

BEGIN
IF (EvalStr(itemHdl, R IN [kLIRecName])=TrueStr) THEN
	BEGIN {Don't attempt to search for it unless it has the LIR}
	tempStr := Concat('(NOTINREFDLVP & NOTINDLVP & (PON=''',kIObName,'''))');
	testCount := SearchForAcc('',symName,tempStr);
	END;
```
```python
result = vs.EvalStr(h, c)
```

## Version
Availability: from All Versions

## Category
* [Criteria](../Categories/Criteria.md)
