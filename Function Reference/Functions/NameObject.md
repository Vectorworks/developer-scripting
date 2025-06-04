# NameObject

## Description
Procedure NameObject assigns an object name to the next object created.

```pascal
PROCEDURE NameObject(objName : STRING);
```

```python
def vs.NameObject(objName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objName|STRING|Name to be assigned to object.|

## Examples
#### VectorScript ####
```pascal
NameObject('Part 5257');
Rect(0,2,2,0);
```
On Vectorworks 2009 the function have problems with groups ([[VS:BeginGroup]] and [[VS:EndGroup]]). In order to workaround the problem use this ([[VS:SetName]] call):
```pascal
BeginGroup;
Rect(0,2,2,0);
EndGroup;
SetName(LNewObj, 'Part 5257');
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [Object Names](../Categories/Object%20Names.md)
