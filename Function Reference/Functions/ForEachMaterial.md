# ForEachMaterial

## Description
Enumerate the materials in the current file.

```pascal
PROCEDURE ForEachMaterial(
				onlyUsed : BOOLEAN;
				callback : PROCEDURE);
```

```python
def vs.ForEachMaterial(onlyUsed, callback):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|onlyUsed|BOOLEAN|List only materials that are used in the current file.|
|callback|PROCEDURE|Callback to be executed for each material in the file, or for each material that is used, depending on the 'used' parameter.|

## Version
Availability: from Vectorworks 2021

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
