# DisplayContextHelpOfCurrentPlugin

## Description
This function will display the context help of the plug-in that is considered ?current?. This could be a command plug-in that has a dialog open, or a tool plug-in that is active.

```pascal
PROCEDURE DisplayContextHelpOfCurrentPlugin;
```

```python
def vs.DisplayContextHelpOfCurrentPlugin():
    return None
```

## Examples
```pascal
DisplayContextHelpOfCurrentPlugin;
```
```python
import vs

# This could be a command plug-in that has a dialog open, or a tool plug-in
# that is active.
vs.DisplayContextHelpOfCurrentPlugin()
```

## Version
Availability: from VectorWorks12.0

## Category
* [Utility](../Categories/Utility.md)
