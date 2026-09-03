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

#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	ok : BOOLEAN;
BEGIN
	ok := IFC_DMDeleteEntry('Wall', 'IfcWall');
END;

RUN(Test);
```
#### Python ####
```python
ok = vs.IFC_DMDeleteEntry('Wall', 'IfcWall')
```

```pascal
resultOK := IFC_DMDeleteEntry('Example', 'Example');
```
```python
import vs

# Deletes an Еntry group from indicated object, from current IFC Data Mapping.
inStrObjName = 'Example'
inStrEntryName = 'Example'

ok = vs.IFC_DMDeleteEntry(inStrObjName, inStrEntryName)
if ok:
    vs.Message('IFC_DMDeleteEntry succeeded')
else:
    vs.Message('IFC_DMDeleteEntry failed')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
