# IsLDSchematicViewObj

## Description
Check if the handle is a schematic view object.

```pascal
FUNCTION IsLDSchematicViewObj(handle : HANDLE): BOOLEAN;
```

```python
def vs.IsLDSchematicViewObj(handle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |

## Examples
```pascal
BEGIN
	IF IsLDSchematicViewObj(InstHandle) THEN
	BEGIN
		schematicViewName := 'NNA_SchematicViewObject';
		SetRField(InstHandle, schematicViewName, 'SchematicUseLegend', LegendName);
		SetRField(InstHandle, schematicViewName, 'SchematicUseCustomLegend', 'TRUE');
	END
```
```python
import vs

# Check if the handle is a schematic view object.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.IsLDSchematicViewObj(handle)
if ok:
    vs.Message('IsLDSchematicViewObj succeeded')
else:
    vs.Message('IsLDSchematicViewObj failed')
```

## Version
Availability: from Vectorworks 2025

## Category
* [Spotlight](../Categories/Spotlight.md)
