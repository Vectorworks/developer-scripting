# IFC_GetExportPhase

## Description
Returns the IFC export phase specified in the Export dialog. If no phase is selected, the active phase is returned.

```pascal
FUNCTION IFC_GetExportPhase(VAR outExportPhase : STRING) : BOOLEAN;
```

```python
def vs.IFC_GetExportPhase():
    return (BOOLEAN, outExportPhase)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outExportPhase|STRING||

## Version
Availability: from Vectorworks 2026.4

## Category
* [IFC](Categories/IFC.md)

