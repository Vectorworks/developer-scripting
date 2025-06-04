# MoveObjs

## Description
Procedure MoveObjs moves object(s) a specified offset distance. The last two parameters, allLayers and allObjects,  control which objects are offset by this procedure.

{| class="wikitable_c"
|+ Table - Effect of MoveObjs Parameters
! allLayers !! allObjects !! Effect
|-
| TRUE
| TRUE
| Move all objects on all layers
|-
| TRUE
| FALSE
| Move selected objects on all layers
|-
| FALSE
| TRUE
| Move all objects on active layer
|-
| FALSE
| FALSE
| Move selected objects on active layer
|}

```pascal
PROCEDURE MoveObjs(
				move       : REAL;
				allLayers  : BOOLEAN;
				allObjects : BOOLEAN);
```

```python
def vs.MoveObjs(move, allLayers, allObjects):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|move|REAL|X-Y object offset distance.|
|allLayers|BOOLEAN|Move objects on all layers option setting.|
|allObjects|BOOLEAN|Move all objects option setting.|

## Examples
#### VectorScript ####
```pascal
MoveObjs(3,0,FALSE,FALSE);
{ moves selected objects on active layer 3 units to the right }
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [Object Editing](../Categories/Object%20Editing.md)
