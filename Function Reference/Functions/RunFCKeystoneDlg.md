# RunFCKeystoneDlg

## Description
Spawns dialog for four corner keystoning

```pascal
FUNCTION RunFCKeystoneDlg(
				handle           : HANDLE;
				VAR keystoneMode : INTEGER;
				VAR vKeystone    : REAL;
				VAR topLeft      : VECTOR;
				VAR topRight     : VECTOR;
				VAR botLeft      : VECTOR;
				VAR botRight     : VECTOR) : BOOLEAN;
```

```python
def vs.RunFCKeystoneDlg(handle, keystoneMode, vKeystone, topLeft, topRight, botLeft, botRight):
    return (BOOLEAN, keystoneMode, vKeystone, topLeft, topRight, botLeft, botRight)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE||
|keystoneMode|INTEGER||
|vKeystone|REAL||
|topLeft|VECTOR||
|topRight|VECTOR||
|botLeft|VECTOR||
|botRight|VECTOR||

## Version
Availability: from Vectorworks 2027

## Category
* [Spotlight](Categories/Spotlight.md)

