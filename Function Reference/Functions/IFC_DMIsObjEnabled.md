# IFC_DMIsObjEnabled

## Description
Returns a flag that shows whether the provided object is enabled in the current mapping settings.

```pascal
FUNCTION IFC_DMIsObjEnabled(inStrObjName : STRING): BOOLEAN;
```

```python
def vs.IFC_DMIsObjEnabled(inStrObjName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|Object's name.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE IsObjEnabled;
VAR
	bOk : BOOLEAN;
BEGIN
	bOk := IFC_DMIsObjEnabled('Space'); {bOk returns if the Space Object is enabled in the current mapping}
END;

RUN(IsObjEnabled);
```
#### Python ####
```python
bOk = vs.IFC_DMIsObjEnabled('Space'); #bOk returns if the Space Object is enabled in the current mapping
```

## See Also
[IFC_DMEnableObject](IFC_DMEnableObject.md)

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
