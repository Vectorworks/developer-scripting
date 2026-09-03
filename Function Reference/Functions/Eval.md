# Eval

## Description
Evaluates whether an object meets the specified search criteria. 

When used with record criteria, it will determine whether a specific record is attached to the object; if used with record-field criteria, it will return the value of the field as a REAL value.

```pascal
FUNCTION Eval(
				h : HANDLE;
				c : CRITERIA): REAL;
```

```python
def vs.Eval(h, c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle of object to which the search criteria will be applied.|
|c|CRITERIA|Search criteria.|

## Examples
#### VectorScript ####
```pascal
hasRecord:=Eval(handleToObject,(R IN ['Part Info']);
```
#### Python ####
```python

```

```pascal
BEGIN
	if handle_cnt < 32767 then BEGIN
		ok := (SQL = '((ALL))') | (Eval(h, sql) > 0);
		IF (ok) & (lineweightDo) & (lineweightVa <> mT) THEN BEGIN
			if not ObjectHasLW(h) then ok := false else BEGIN
				num1 := GetLW(h);
				num2 := Str2Num(lineweightVa);

IF ( kGroup = nType ) THEN
	TraverseGroups( FInGroup( h ), bFMOnly )
ELSE IF ( (kPlugInObject = nType) ) THEN BEGIN
	IF ( bFMOnly ) THEN BEGIN
		bReplace := ( 0 < Eval( h, (R IN [ kStrFM ]) ) );
	END

BEGIN
	for cnt1 := 1 to NumRecords(source) do BEGIN
		recHand := GetRecord(source, cnt1);
		recName := GetName(recHand);
		IF Eval(target, (R IN [recName])) = 0 THEN SetRecord(target, recName);
		for cnt2 := 1 to NumFields(recHand) do BEGIN
			fldName := GetFldName(recHand, cnt2);
			SetRField(target, recName, fldName, GetRField(source, recName, fldName));
		END;
```
```python
result = vs.Eval(h, c)
```

## Version
Availability: from All Versions

## Category
* [Criteria](../Categories/Criteria.md)
