# ResList_InitDef

## Description
Initialize a categories resource with red symbol resources of the specified universal name. The 'uniqueID' is a string identifier uniquely identifying this control.

```pascal
PROCEDURE ResList_InitDef(
				uniqueID : STRING;
				univName : STRING);
```

```python
def vs.ResList_InitDef(uniqueID, univName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |
|univName|STRING|   |

## Examples
```pascal
ResList_InitDef('Example', 'Example');
```
```python
import vs

# Initialize a categories resource with red symbol resources of the specified
# universal name.
uniqueID = 'Example'
univName = 'Example'

vs.ResList_InitDef(uniqueID, univName)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
