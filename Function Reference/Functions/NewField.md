# NewField

## Description
Creates a new field in a specified record format. If the record does not exist, a new one is created using the specified record name.

Please refer to the [[VS:Function Reference Appendix#Record - Worksheet Field Types|VectorScript Appendix]] for specific field data types and formatting.

```pascal
PROCEDURE NewField(
				recName    : STRING;
				fieldName  : STRING;
				fieldValue : DYNARRAY[] of CHAR;
				fType      : INTEGER;
				fFlag      : INTEGER);
```

```python
def vs.NewField(recName, fieldName, fieldValue, fType, fFlag):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|recName|STRING|Name of record to which field will be added.|
|fieldName|STRING|Name of new field.|
|fieldValue|DYNARRAY[] of CHAR|Default value for new field.|
|fType|INTEGER|Data type of new field.|
|fFlag|INTEGER|Display style of field.|

## Remarks
If the fieldName argument is longer than 20 characters, it will be truncated to 20 characters, without warning. The recName argument can be up to something like 60 characters (I think).

## Examples
==== VectorScript ====
```pascal
NewField('Part Info','Serial No.','A-0000',4,0);
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
