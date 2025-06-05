# SetTool

## Description
Activates the specified VectorWorks tool for use. The tool remains selected as the active tool after use.

Note: Please refer to the [Script Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#settool---calltool-selectors) for specific tool ID values.

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
