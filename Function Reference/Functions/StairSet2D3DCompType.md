# StairSet2D3DCompType

## Description
<lineList ident=2>
<line>
Sets 2D3D components type of stair - not recommended for use
</line>
<line>
1: 2D
</line>
<line>
2: Hybrid
</line>
<line>
See SDKLib/Include/Interfaces/Vectorworks/Extension/IStairCWSupport.h for more details.
</line>
</lineList>

```pascal
FUNCTION StairSet2D3DCompType(
				stair             : HANDLE;
				ComponentType2D3D : INTEGER): BOOLEAN;
```

```python
def vs.StairSet2D3DCompType(stair, ComponentType2D3D):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stair|HANDLE|   |
|ComponentType2D3D|INTEGER|   |

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
