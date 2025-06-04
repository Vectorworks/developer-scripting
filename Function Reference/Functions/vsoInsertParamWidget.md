# vsoInsertParamWidget

## Description
Inserts a widget into the OI palette.

See the <a href=http://www.vectorlab.info/index.php?title=Events>VectorLab article</a> on object events.

```pascal
FUNCTION vsoInsertParamWidget(
				position    : LONGINT;
				parameterID : LONGINT;
				text        : STRING;
				data        : LONGINT):BOOLEAN;
```

```python
def vs.vsoInsertParamWidget(position, parameterID, text, data):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|position|LONGINT|   |
|parameterID|LONGINT|   |
|text|STRING|   |
|data|LONGINT|   |

## Remarks
This function inserts a widget into the OIP. Unlike the vsoAppendParamWidget which just appends the widget to the end of the OIP, this call allows the user to define the position in the OIP parameter list.

position: the position in OIP parameter list to insert the widget.
parameterID: the corresponding ordinal value of the parameter in the object's parameter list.

text:  the widget label.
data:  not implemented yet.

## Examples
==== VectorScript ====
```pascal
If GetLocalizedPluginParameter('NewModelWindowMain','TopShape',temp_s) then
Begin
   result := vsoInsertParamWidget(1,1,temp_s,eventData);
end;
```
==== Python ====
```python

```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
