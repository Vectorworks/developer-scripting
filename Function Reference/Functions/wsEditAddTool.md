# wsEditAddTool

## Description
Add a menu under Third-party palette and companyName tool set.

**Table - Tool Types**

| Tool Type                | Constant |
|--------------------------|----------|
| Regular External Tool    | 1        |
| VectorScript Tool (.vst) | 2        |
| VectorScript Object (.vso)| 3       |
| Custom Parametric        | 4        |

*Note:* The Custom Parametric tool type includes SDK objects of type Point, Line, Box, 2D Path, and 3D Path.

```pascal
PROCEDURE wsEditAddTool(
				toolName : STRING;
				toolType : INTEGER);
```

```python
def vs.wsEditAddTool(toolName, toolType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|toolName|STRING|   |
|toolType|INTEGER|   |

## Remarks
As of Vectorworks 2018 SP2, this function takes an integer parameter toolType to specify the type of tool being added. Vectorworks 2018 prior to SP2 will only take a single parameter as input.

## Version
Availability: from Vectorworks 2018

## Category
* [Workspaces](../Categories/Workspaces.md)
