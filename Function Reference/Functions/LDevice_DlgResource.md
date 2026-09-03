# LDevice_DlgResource

## Description
Sets the Lightning Device Resource selector in the pointed field

```pascal
PROCEDURE LDevice_DlgResource(
				LayoutID   : INTEGER;
				ControlID  : INTEGER;
				SymbolName : STRING);
```

```python
def vs.LDevice_DlgResource(LayoutID, ControlID, SymbolName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|LayoutID|INTEGER|   |
|ControlID|INTEGER|   |
|SymbolName|STRING|   |

## Examples
```pascal
LDevice_DlgResource( AddEditLegend, kSelSymResource, gSelectedSymbolName );
{Initialize the rows to be used in kFieldsLB.}
EnableLBColumnLines(AddEditLegend, kFieldsLB, TRUE);
SetLBSortColumn(AddEditLegend, kFieldsLB, kColNumber, FALSE);
```
```python
import vs

# Sets the Lightning Device Resource selector in the pointed field.
LayoutID = 1
ControlID = 2
SymbolName = 'MySymbol'

vs.LDevice_DlgResource(LayoutID, ControlID, SymbolName)
```

## Version
Availability: from Vectorworks 2019

## Category
* [Spotlight](../Categories/Spotlight.md)
