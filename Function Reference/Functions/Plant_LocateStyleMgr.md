# Plant_LocateStyleMgr

## Description
Locate the selected plant's style in the Plant Style Manager, and make the palette visible

```pascal
PROCEDURE Plant_LocateStyleMgr(plant : HANDLE);
```

```python
def vs.Plant_LocateStyleMgr(plant):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|plant|HANDLE||

## Examples
```pascal
Plant_LocateStyleMgr(plant);
```
```python
import vs

# Locate the selected plant's style in the Plant Style Manager, and make the
# palette visible.
plant = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.Plant_LocateStyleMgr(plant)
```

## Version
Availability: from Vectorworks 2026

## Category
* [PlantObjectCoreTools](../Categories/PlantObjectCoreTools.md)
