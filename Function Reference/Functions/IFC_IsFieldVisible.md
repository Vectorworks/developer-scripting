# IFC_IsFieldVisible

## Description
Gets field visibility state for Data Sheet: &lt;Default Settings&gt; on OIP Data Pane.

```pascal
FUNCTION IFC_IsFieldVisible(
				objectName     : STRING;
				mainEntry      : STRING;
				childEntry     : STRING;
				fieldName      : STRING;
				VAR outVisible : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_IsFieldVisible(objectName, mainEntry, childEntry, fieldName):
    return (BOOLEAN, outVisible)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|mainEntry|STRING|   |
|childEntry|STRING|   |
|fieldName|STRING|   |
|outVisible|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_IsFieldVisible('Example', 'Example', 'Example', 'MyRecord', TRUE);
```
```python
import vs

# Gets field visibility state for Data Sheet: &lt;Default Settings&gt; on OIP
# Data Pane.
objectName = 'Example'
mainEntry = 'Example'
childEntry = 'Example'
fieldName = 'MyField'

ok, outVisible = vs.IFC_IsFieldVisible(objectName, mainEntry, childEntry, fieldName)
vs.Message('IFC_IsFieldVisible returned: ' + str((ok, outVisible)))
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
