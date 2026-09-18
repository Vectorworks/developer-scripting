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

## Examples
```pascal
ForEachMaterial(TRUE, callback);
```
```python
import vs

# Enumerate the materials in the current file.
def handle_object(objHandle):
    vs.Message('Processing: ' + str(objHandle))

onlyUsed = True
callback = handle_object

vs.ForEachMaterial(onlyUsed, callback)
```

## Version
Availability: from Vectorworks 2021

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
