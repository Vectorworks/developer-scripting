# StairSetConstType

## Description
<lineList ident=2>
<line>
Sets construction type of stair - not recommended for use
</line>
<line>
1: Solid
</line>
<line>
2: Stringer underneath
</line>
<line>
3: Stringer outside
</line>
<line>
4: Concrete 
</line>
<line>
5: CircularWithTangentialSteps /* Special type used by circular stairs only */
</line>
<line>
See SDKLib/Include/Interfaces/Vectorworks/Extension/IStairCWSupport.h for more details.
</line>

</lineList>

```pascal
FUNCTION StairSetConstType(
				stair            : HANDLE;
				ConstructionType : INTEGER): BOOLEAN;
```

```python
def vs.StairSetConstType(stair, ConstructionType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stair|HANDLE|   |
|ConstructionType|INTEGER|   |

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
