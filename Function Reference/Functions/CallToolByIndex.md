# CallToolByIndex

## Description
Similar to CallTool. Takes the internal ID of a tool ([[VS:Function_Reference_Appendix#settool| Appendix]] )

```pascal
FUNCTION CallToolByIndex(toolIndex : INTEGER): BOOLEAN;
```

```python
def vs.CallToolByIndex(toolIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|toolIndex|INTEGER|   |

## Examples
#### VectorScript ####
```pascal
Message( CallToolByIndex( -221 ) ) { activate locus tool, returns true if successful }
```
#### Python ####
```python
vs.Message( vs.CallToolByIndex( -221 ) ) # activate locus tool, returns true if successful
```

## See Also
VS Functions:
* [CallTool](CallTool.md)
* [CallToolByName](CallToolByName.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
