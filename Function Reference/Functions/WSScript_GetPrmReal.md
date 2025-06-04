# WSScript_GetPrmReal

## Description
This function must be used inside a worksheet script called by 'RunScript' worksheet formula.

```pascal
FUNCTION WSScript_GetPrmReal(paramIndex : INTEGER): REAL;
```

```python
def vs.WSScript_GetPrmReal(paramIndex):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|paramIndex|INTEGER|Zero based index of the parameter passed to the RunScript worksheet function.|

## See Also
VS Functions:
[WSScript_GetObject](WSScript_GetObject.md) 
| [WSScript_GetPrmInt](WSScript_GetPrmInt.md) 
| [WSScript_GetPrmReal](WSScript_GetPrmReal.md) 
| [WSScript_GetPrmStr](WSScript_GetPrmStr.md) 
| [WSScript_SetResStr](WSScript_SetResStr.md) 
| [WSScript_SetResReal](WSScript_SetResReal.md) 
| [WSScript_SetResImage](WSScript_SetResImage.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Worksheets](../Categories/Worksheets.md)
