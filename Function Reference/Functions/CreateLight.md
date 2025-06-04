# CreateLight

## Description
CreateLight creates a new light object in the active VectorScript document. 

A new light objects' color is defaulted to white, and brightness is defaulted to 75%. 

{| class="wikitable_c"
|+ Table - Light Types
! Light Type !! Constant
|-
| Directional
| 0
|-
| Point
| 1
|-
| Spot
| 2
|}

```pascal
FUNCTION CreateLight(
				pXR        : REAL;
				pYR        : REAL;
				pZR        : REAL;
				lightType  : INTEGER;
				isOn       : BOOLEAN;
				castShadow : BOOLEAN): HANDLE;
```

```python
def vs.CreateLight(pXR, pYR, pZR, lightType, isOn, castShadow):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pXR|REAL|X coordinate of new light.|
|pYR|REAL|Y coordinate of new light.|
|pZR|REAL|Z coordinate of new light.|
|lightType|INTEGER|Light type.|
|isOn|BOOLEAN|On-off status of light.|
|castShadow|BOOLEAN|Specifies whether light will cast shadow.|

## Examples
#### VectorScript ####
```pascal
CreateLight(2, 3, 8, 1, TRUE, TRUE);
```
#### Python ####
```python
vs.CreateLight(2, 3, 8, 1, True, True)
```

## Version
Availability: from MiniCAD 7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
