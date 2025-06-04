# SetWInsLocOffByStyle

## Description
Sets whether the wall insert location offset of a symbol definition, plug-in object style, or plug-in object is by style.

```pascal
FUNCTION SetWInsLocOffByStyle(
				hObject : HANDLE;
				byStyle : BOOLEAN): BOOLEAN;
```

```python
def vs.SetWInsLocOffByStyle(hObject, byStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|
|byStyle|BOOLEAN|Whether the wall insert location offset is by style.|

## See Also
VS Functions:
[GetWInsLocOffByStyle](GetWInsLocOffByStyle.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
