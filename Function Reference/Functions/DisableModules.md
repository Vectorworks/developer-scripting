# DisableModules

## Description
Disables modules.  The modules parameter is a bitfield indicating which modules to disable.

* Table - GetEnabledModules Selectors

| Module | Selector | Description |
|---|---|---|
| Foundation | 0 | VectorWorks general purpose CAD. |
| RenderWorks | 1 | Advanced rendering features, lighting, textures. |
| Architect | 2 | Architectural features including advanced window, door, wall framing, HVAC |
| Landmark | 4 | Site modeling and landscape design module. |
| Spotlight | 8 | Theater lighting, set, and scenic design features. |
| Mechanical | 16 | Mechanical engineering module for designers and fabricators. |
| Pro | 32 | Foundation for European market. |

```pascal
PROCEDURE DisableModules(modules : LONGINT);
```

```python
def vs.DisableModules(modules):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|modules|LONGINT|This modules parameter is a LONGINT value which contains a bit for each possible product module.  If a module is enabled, then the corresponding bit is set to 1.  If that module is disabled, then its bit is 0.  The table below contains selectors that can be used to interpret the results of this function.  To determine if a module is enabled, do a bitwise &quot;and&quot; operation with the selector and the value returned by this function.  See the usage example below.|

## See Also
VS Functions:
[GetEnabledModules](GetEnabledModules.md)

## Version
Availability: from VectorWorks 10.0

## Category
* [Utility](../Categories/Utility.md)
