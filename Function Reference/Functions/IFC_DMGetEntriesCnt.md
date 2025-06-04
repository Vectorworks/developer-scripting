# IFC_DMGetEntriesCnt

## Description
Gets the count of entries for indicated object from current IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetEntriesCnt(
				inStrObjName : STRING;
				VAR outCount : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMGetEntriesCnt(inStrObjName):
    return (BOOLEAN, outCount)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|Object name.|
|outCount|INTEGER|Returns IfcEntity groups count from IFC Data Mapping.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE GetEntriesCnt;
VAR
    cnt  : INTEGER;
BEGIN
    IF IFC_DMGetEntriesCnt('Space', cnt) THEN
        AlrtDialog(Concat('Count of Entries: ', cnt));
END;
RUN(GetEntriesCnt);
```
#### Python ####
```python
cnt = 0
boo, cnt = vs.IFC_DMGetEntriesCnt('Space', cnt)
if boo:
    vs.AlrtDialog(f"Count of Entries: {cnt}")
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
