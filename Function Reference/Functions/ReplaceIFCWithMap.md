# ReplaceIFCWithMap

## Description
Deletes attached IFC Record from:

case 1: Object If the HANDLE is not NULL.

case 2: All Objects which corresponds to inStrObjName and HANDLE is NULL.

case 3: All Objects if inStrObjName is "allObjects" and HANDLE is NULL.

```pascal
FUNCTION ReplaceIFCWithMap(
				hObject      : HANDLE;
				inStrObjName : STRING): BOOLEAN;
```

```python
def vs.ReplaceIFCWithMap(hObject, inStrObjName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Object's Handle.|
|inStrObjName|STRING|Object name.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	ok : BOOLEAN;
BEGIN
	ok := ReplaceIFCWithMap(NIL, 'Wall');
END;

RUN(Test);
```
#### Python ####
```python
ok = vs.ReplaceIFCWithMap(NULL, 'Wall')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
