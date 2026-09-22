# GetProjData

## Description
Gets projector data from light node

```pascal
FUNCTION GetProjData(
				handle               : HANDLE;
				VAR outFloorMounted  : BOOLEAN;
				VAR outAspectRatio   : REAL;
				VAR outKeystoneColor : VECTOR;
				VAR outKeystoneRow0  : VECTOR;
				VAR outKeystoneRow1  : VECTOR;
				VAR outKeystoneRow2  : VECTOR) : BOOLEAN;
```

```python
def vs.GetProjData(handle):
    return (BOOLEAN, outFloorMounted, outAspectRatio, outKeystoneColor, outKeystoneRow0, outKeystoneRow1, outKeystoneRow2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE||
|outFloorMounted|BOOLEAN||
|outAspectRatio|REAL||
|outKeystoneColor|VECTOR||
|outKeystoneRow0|VECTOR||
|outKeystoneRow1|VECTOR||
|outKeystoneRow2|VECTOR||

## Version
Availability: from Vectorworks 2027

## Category
* [Spotlight](Categories/Spotlight.md)

