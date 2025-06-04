# SetTool

## Description
Activates the specified VectorWorks tool for use. The tool remains selected as the active tool after use.

Note: Please refer to the [[VS:Function Reference Appendix#SetTool - CallTool Selectors|VectorScript Appendix]] for specific tool ID values.

```pascal
PROCEDURE SetTool(theTool : INTEGER);
```

```python
def vs.SetTool(theTool):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theTool|INTEGER|VectorWorks tool constant.|

## Examples
#### VectorScript ####
```pascal
SetTool(-203);
```
#### Python ####
```python
vs.SetTool(-241)
```

## See Also
VS Functions:
[CallTool](CallTool.md)

## Version
Availability: from All Versions

## Category
* [Command](../Categories/Command.md)
