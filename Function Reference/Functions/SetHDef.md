# SetHDef

## Description
Procedure SetHDef replaces the definition of the referenced &quot;container&quot; object with a new definition. Supported object types are worksheets, symbol definitions, and layer references.

```pascal
PROCEDURE SetHDef(
				oldH : HANDLE;
				newH : HANDLE);
```

```python
def vs.SetHDef(oldH, newH):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|oldH|HANDLE|Handle to object.|
|newH|HANDLE|Handle to new definition.|

## Examples
#### VectorScript ####
```pascal
SetHDef(symbolHd,newSymDefHd);
{updates the referenced symbol with a new definition}
```
#### Python ####
```python

```

## Version
Availability: from MiniCAD6.0

## Category
* [Object Editing](../Categories/Object%20Editing.md)
