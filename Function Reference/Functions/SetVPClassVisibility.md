# SetVPClassVisibility

## Description
Sets the visibility for the specified class in the specified viewport.

```pascal
FUNCTION SetVPClassVisibility(
				viewportHandle : HANDLE;
				className      : STRING;
				visibilityType : INTEGER): BOOLEAN;
```

```python
def vs.SetVPClassVisibility(viewportHandle, className, visibilityType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|   |
|className|STRING|   |
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
