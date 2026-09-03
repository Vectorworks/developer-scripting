# vsoStyleWidgetChoice

## Description
Get the item chosen in the Plug-in Object Style widget.

```pascal
PROCEDURE vsoStyleWidgetChoice(VAR choice : INTEGER);
```

```python
def vs.vsoStyleWidgetChoice():
    return choice
```

## Parameters
|Name|Type|Description|
|---|---|---|
|choice|INTEGER|   |

## Examples
```pascal
vsoStyleWidgetChoice(1);
```
```python
import vs

# Get the item chosen in the Plug-in Object Style widget.
result = vs.vsoStyleWidgetChoice()
```

## Version
Availability: from Vectorworks 2017

## Category
* [Object Events](../Categories/Object%20Events.md)
