# GetParamStyleType

## Description
Returns the style type (by instance or by style) for a parameter.

```pascal
FUNCTION GetParamStyleType(
				hStyle    : HANDLE;
				paramName : STRING): INTEGER;
```

```python
def vs.GetParamStyleType(hStyle, paramName):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hStyle|HANDLE|Handle to a symbol containing a plug-in style.|
|paramName|STRING|Universal name of a parameter to check for style type.|

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
