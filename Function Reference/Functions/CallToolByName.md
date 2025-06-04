# CallToolByName

## Description
Similar to CallTool, but takes name rather than ID. Supports plug-in tools (but not yet internal tools).

```pascal
FUNCTION CallToolByName(toolName : STRING): BOOLEAN;
```

```python
def vs.CallToolByName(toolName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|toolName|STRING|   |

## Examples
==== VectorScript ====
```pascal
Message( CallToolByName( 'Spiral' ) );
{ activates Spiral tool, returns true if successful
Note: Spiral is not an internal tool
if you try it for example with 'Wall' this will return an error, since it's an internal tool }
```
==== Python ====
```python
vs.Message( vs.CallToolByIndex( 'Spiral' ) ) 
# activates Spiral tool, returns true if successful
# Note: Spiral is not an internal tool
# if you try it for example with 'Wall' this will return an error, since it's an internal tool
```

## See Also
VS Functions:
* [CallTool](CallTool.md)
* [CallToolByIndex](CallToolByIndex.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
