# BeginModeButtonsText

## Description
Creates a mode bar buttons help text.

```pascal
PROCEDURE BeginModeButtonsText;
```

```python
def vs.BeginModeButtonsText():
    return None
```

## Examples
```pascal
BeginModeButtonsText;
SetModeButtonText( 'Mode1', 1 );
SetModeButtonText( 'Mode2', 0 );
EndModeButtonsText;
```

```pascal
BeginModeButtonsText;
```
```python
import vs

# Creates a mode bar buttons help text.
vs.BeginModeButtonsText()
newObj = vs.LNewObj()  # handle to the newly created object
```

## See Also
VS Functions:
[EndModeButtonsText](EndModeButtonsText.md) 
| [SetModeButtonText](SetModeButtonText.md)

## Version
Availability: from Vectorworks 2013

## Category
* [User Interactive](../Categories/User%20Interactive.md)
