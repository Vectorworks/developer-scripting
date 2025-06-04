# SetVPLayerVisibility

## Description
Sets the visibility for the specified layer in the specified viewport.

```pascal
FUNCTION SetVPLayerVisibility(
				viewportHandle : HANDLE;
				layerHandle    : HANDLE;
				visibilityType : INTEGER): BOOLEAN;
```

```python
def vs.SetVPLayerVisibility(viewportHandle, layerHandle, visibilityType):
    return BOOLEAN
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
