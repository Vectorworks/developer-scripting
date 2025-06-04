# IFC_SetFieldVisible

## Description
Sets field visibility state for Data Sheet: &lt;Default Settings&gt; on OIP Data Pane.

```pascal
FUNCTION IFC_SetFieldVisible(
				objectName : STRING;
				mainEntry  : STRING;
				childEntry : STRING;
				fieldName  : STRING;
				isVisible  : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_SetFieldVisible(objectName, mainEntry, childEntry, fieldName, isVisible):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|mainEntry|STRING|   |
|childEntry|STRING|   |
|fieldName|STRING|   |
|isVisible|BOOLEAN|   |

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
