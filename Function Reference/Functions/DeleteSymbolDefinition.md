# DeleteSymbolDefinition

## Description
Procedure DeleteSymbolDefinition deletes the referenced symbol definition from the document.  If bCompletely is TRUE, all corresponding symbol instances will be deleted completely; otherwise, the symbol instances will be replaced with loci.

```pascal
PROCEDURE DeleteSymbolDefinition(
				hSymDef     : HANDLE;
				bCompletely : BOOLEAN);
```

```python
def vs.DeleteSymbolDefinition(hSymDef, bCompletely):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hSymDef|HANDLE|Handle to the symbol definition.|
|bCompletely|BOOLEAN|Determines whether to replace the corresponding symbol instances with loci or delete the instances completely.|

## Version
Availability: from Vectorworks 2011

## Category
* [Object Editing](../Categories/Object%20Editing.md)
