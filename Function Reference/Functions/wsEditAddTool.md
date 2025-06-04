# wsEditAddTool

## Description
Add a menu under Third-party palette and companyName tool set.


{| class="wikitable_c"
! Tool Type !! Constant
|-
| Regular External Tool
| style="text-align:center"| 1
|-
| VectorScript Tool (.vst)
| style="text-align:center"| 2
|-
| VectorScript Object (.vso)
| style="text-align:center"| 3
|-
| Custom Parametric
| style="text-align:center"| 4
|}

<i>Note:</i> The Custom Parametric tool type includes SDK objects of type Point, Line, Box, 2D Path, and 3D Path.

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
