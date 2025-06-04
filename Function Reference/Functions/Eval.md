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

## Version
Availability: from All Versions

## Category
* [Criteria](../Categories/Criteria.md)
