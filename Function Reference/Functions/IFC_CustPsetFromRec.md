# IFC_CustPsetFromRec

## Description
Creates custom property set from a record

```pascal
FUNCTION IFC_CustPsetFromRec(hRecord : HANDLE) : BOOLEAN;
```

```python
def vs.IFC_CustPsetFromRec(hRecord):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hRecord|HANDLE||

## Examples
```pascal
resultOK := IFC_CustPsetFromRec(hRecord);
```
```python
import vs

# Creates custom property set from a record.
hRecord = vs.GetObject('MyRecord')  # handle to a record format

ok = vs.IFC_CustPsetFromRec(hRecord)
if ok:
    vs.Message('IFC_CustPsetFromRec succeeded')
else:
    vs.Message('IFC_CustPsetFromRec failed')
```

## Version
Availability: from Vectorworks 2026.1

## Category
* [IFC](../Categories/IFC.md)
