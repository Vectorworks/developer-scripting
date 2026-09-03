# IFC_DMLoadSettings

## Description
Loads the indicated IFC Data Mapping to Document.

```pascal
FUNCTION IFC_DMLoadSettings(inStrParam : STRING): BOOLEAN;
```

```python
def vs.IFC_DMLoadSettings(inStrParam):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrParam|STRING|IFC Data Mapping name. If parameter is Empty, it's going to load the Default IFC Data Mapping.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	ok : BOOLEAN;
BEGIN
	ok := IFC_DMLoadSettings('MyIFCMapping');
END;

RUN(Test);
```
#### Python ####
```python
ok = vs.IFC_DMLoadSettings('MyIFCMapping')
```

```pascal
resultOK := IFC_DMLoadSettings('Example');
```
```python
import vs

# Loads the indicated IFC Data Mapping to Document.
inStrParam = 'Example'

ok = vs.IFC_DMLoadSettings(inStrParam)
if ok:
    vs.Message('IFC_DMLoadSettings succeeded')
else:
    vs.Message('IFC_DMLoadSettings failed')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
