# IFC_DMDeleteEntry

## Description
Deletes an Еntry group from indicated object, from current IFC Data Mapping.

```pascal
FUNCTION IFC_DMDeleteEntry(
				inStrObjName   : STRING;
				inStrEntryName : STRING): BOOLEAN;
```

```python
def vs.IFC_DMDeleteEntry(inStrObjName, inStrEntryName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|Object Name.|
|inStrEntryName|STRING|Ifc Entry group name.|

## Examples
Assume we want to clear "IfcWall" Entry Group from the mapping for Wall Object:

==== VectorScript ====
```pascal
PROCEDURE Test;
VAR
	ok : BOOLEAN;
BEGIN
	ok := IFC_DMDeleteEntry('Wall', 'IfcWall');
END;

RUN(Test);
```
==== Python ====
```python
ok = vs.IFC_DMDeleteEntry('Wall', 'IfcWall')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
