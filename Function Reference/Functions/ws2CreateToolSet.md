# ws2CreateToolSet

## Description
Workspace advanced APIs. Create a new tool set if it doesn't exist. Retina icon will be loaded automatically if it has the same name suffixed with @2x.png and resolution 26 by 20 pixels.

```pascal
FUNCTION ws2CreateToolSet(
				toolPath         : DYNARRAY[] of CHAR;
				univName         : DYNARRAY[] of CHAR;
				displayName      : DYNARRAY[] of CHAR;
				iconFullFilePath : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.ws2CreateToolSet(toolPath, univName, displayName, iconFullFilePath):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|toolPath|DYNARRAY[] of CHAR|   |
|univName|DYNARRAY[] of CHAR|   |
|displayName|DYNARRAY[] of CHAR|   |
|iconFullFilePath|DYNARRAY[] of CHAR|   |

## Remarks
Starting with Vectorworks 2024 .svg icons are required are required in order to support Dark Mode.
Icon.svg

Icon@2X.svg

Icon_dark.svg

Icon_dark@2X.svg

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
