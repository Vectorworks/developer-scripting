# DisplayContextualHelp

## Description
Using the identifier string for a GUI element given by the Contextual Help Manager displays the associated contextual help. This could be a WebWorks webpage, a Internet webpage or even a local file.

```pascal
FUNCTION DisplayContextualHelp(Identifier : STRING): BOOLEAN;
```

```python
def vs.DisplayContextualHelp(Identifier):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|Identifier|STRING|   |

## Examples
```pascal
BEGIN
	hasHelp := DisplayContextualHelp('net.nemetschek.help.382507DD-8AF6-11E1-B127-842B2B9AB9E0');
END;

BEGIN
	hasHelp := DisplayContextualHelp('net.nemetschek.help.7688AB4D-8AF5-11E1-B127-842B2B9AB9E0');
END;

BEGIN
	hasHelp := DisplayContextualHelp('net.nemetschek.help.3C191F5F-8AF7-11E1-B127-842B2B9AB9E0');
END;
```
```python
import vs

# Using the identifier string for a GUI element given by the Contextual Help
# Manager displays the associated contextual help.
Identifier = 'Example'

ok = vs.DisplayContextualHelp(Identifier)
if ok:
    vs.Message('DisplayContextualHelp succeeded')
else:
    vs.Message('DisplayContextualHelp failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Utility](../Categories/Utility.md)
