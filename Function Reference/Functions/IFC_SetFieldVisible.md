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

## Examples
```pascal
resultOK := IFC_SetFieldVisible('Example', 'Example', 'Example', 'MyRecord', TRUE);
```
```python
import vs

# Sets field visibility state for Data Sheet: &lt;Default Settings&gt; on OIP
# Data Pane.
objectName = 'Example'
mainEntry = 'Example'
childEntry = 'Example'
fieldName = 'MyField'
isVisible = True

ok = vs.IFC_SetFieldVisible(objectName, mainEntry, childEntry, fieldName, isVisible)
if ok:
    vs.Message('IFC_SetFieldVisible succeeded')
else:
    vs.Message('IFC_SetFieldVisible failed')
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
