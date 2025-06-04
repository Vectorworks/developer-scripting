# ValidNumStr

## Description
Function ValidNumStr returns TRUE if the specified string can be converted into a numeric value. If TRUE, the numeric value is returned.

```pascal
FUNCTION ValidNumStr(
				str       : STRING;
				VAR value : REAL): BOOLEAN;
```

```python
def vs.ValidNumStr(str):
    return (BOOLEAN, value)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|str|STRING|String value to be checked for numeric validity.|
|value|REAL|Numeric value converted from input string.|

## Remarks
(Joel Sciamma, 2007.01.13):
* Returns TRUE if the specified string can be converted into a numeric value and places the value in the REAL parameter. 
* Returns FALSE if the specified string can not be converted into a numeric value and places zero in the REAL parameter.

## Examples
#### VectorScript ####
```pascal
CASE Item OF
{// OK Button //}
1:BEGIN
IF ValidNumStr(GetField(4),value) THEN BEGIN
Done:=TRUE;
replaceValue:= GetField(6);

IF ItemSel(9) THEN textMode:=2;
IF ItemSel(10) THEN textMode:=4;
IF ItemSel(11) THEN textMode:=8;
IF ItemSel(12) THEN layerMode:=16;
IF ItemSel(13) THEN layerMode:=32;
IF ItemSel(14) THEN caseMode:=1;
END
ELSE SysBeep;
END;
```
#### Python ####
```python
str = '5m + 5cm'
ok, num = vs.ValidNumStr( str )
vs.AlrtDialog( num )
```

## Version
Availability: from All Versions

## Category
* [Utility](../Categories/Utility.md)
