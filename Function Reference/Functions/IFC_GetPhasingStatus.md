# IFC_GetPhasingStatus

## Description
Returns the IFC status for the object in the specified phase.

```pascal
FUNCTION IFC_GetPhasingStatus(
				hObject          : HANDLE;
				VAR vwPhase      : STRING;
				VAR outIfcStatus : STRING) : BOOLEAN;
```

```python
def vs.IFC_GetPhasingStatus(hObject):
    return (BOOLEAN, vwPhase, outIfcStatus)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE||
|vwPhase|STRING||
|outIfcStatus|STRING||

## Version
Availability: from Vectorworks 2026.4

## Category
* [IFC](Categories/IFC.md)

