# IFC_LGetLocalName

## Description
Returns the Localized Name for the IFC String.

```pascal
FUNCTION IFC_LGetLocalName(
				VAR strIFCName        : STRING;
				VAR inIFCTypeOfString : INTEGER;
				VAR outLocalName      : STRING): BOOLEAN;
```

```python
def vs.IFC_LGetLocalName():
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
