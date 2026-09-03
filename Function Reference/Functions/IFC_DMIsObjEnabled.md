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

```pascal
resultOK := IFC_DMIsObjEnabled('Example');
```
```python
import vs

# Returns a flag that shows whether the provided object is enabled in the
# current mapping settings.
inStrObjName = 'Example'

ok = vs.IFC_DMIsObjEnabled(inStrObjName)
if ok:
    vs.Message('IFC_DMIsObjEnabled succeeded')
else:
    vs.Message('IFC_DMIsObjEnabled failed')
```

## See Also
[IFC_DMEnableObject](IFC_DMEnableObject.md)

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
