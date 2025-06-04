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
[[User:CBM-c-|_c_]], 2015.06.17: 
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

## Version
Availability: from All Versions

## Category
* [Criteria](../Categories/Criteria.md)
