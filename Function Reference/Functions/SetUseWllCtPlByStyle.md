# SetUseWllCtPlByStyle

## Description
Sets whether the use wall cut plane setting of a symbol definition, plug-in object style, or plug-in object is by style.

```pascal
FUNCTION SetUseWllCtPlByStyle(
				hObject : HANDLE;
				byStyle : BOOLEAN) : BOOLEAN;
```

```python
def vs.SetUseWllCtPlByStyle(hObject, byStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|
|byStyle|BOOLEAN|Whether the use wall cut plane setting is by style.|

## Returns
Whether the call succeeded.

## See Also
VS Functions:
[GetUseWllCtPlByStyle](GetUseWllCtPlByStyle.md)

## Version
Availability: from Vectorworks 2026.2

## Category
* [Objects - Custom](Categories/Objects%20-%20Custom.md)

