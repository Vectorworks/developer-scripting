# GetVPLayerVisibility

## Description
Gets the visibility for the specified layer in the specified viewport.

```pascal
FUNCTION GetVPLayerVisibility(
				viewportHandle     : HANDLE;
				layerHandle        : HANDLE;
				VAR visibilityType : INTEGER): BOOLEAN;
```

```python
def vs.GetVPLayerVisibility(viewportHandle, layerHandle):
    return (BOOLEAN, visibilityType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|   |
|layerHandle|HANDLE|   |
|visibilityType|INTEGER|   |

## Remarks
visibilityType values: 
* -1 invisible, 
* 0 visible, 
* 2 gray

## Version
Availability: from VectorWorks 11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
