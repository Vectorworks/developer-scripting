# IFC_LGetUnivName

## Description
Returns the Universal Name for the IFC String.

```pascal
FUNCTION IFC_LGetUnivName(
				VAR strIFCName        : STRING;
				VAR inIFCTypeOfString : INTEGER;
				VAR outLocalName      : STRING): BOOLEAN;
```

```python
def vs.IFC_LGetUnivName():
    return (BOOLEAN, strIFCName, inIFCTypeOfString, outLocalName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strIFCName|STRING|   |
|inIFCTypeOfString|INTEGER|   |
|outLocalName|STRING|   |

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
