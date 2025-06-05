# HideClass

## Description
Sets the class visibility of the specified class to hidden (invisible) status.

```pascal
PROCEDURE HideClass(className : STRING);
```

```python
def vs.HideClass(className):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|

## Remarks
If you're hiding a class for the purpose of printing with that class turned off, you have to do a [ReDrawAll](ReDrawAll.md) before calling the the *[DoMenuTextByName](DoMenuTextByName.md)*('Print',0) call, or else the class doesn't get hidden until after the script completes execution.

## Examples
#### VectorScript ####
```pascal
HideClass('Dimension');
```
#### Python ####
```python
vs.HideClass('Dimension')
```

## See Also
VS Functions:
[ShowClass](ShowClass.md)

## Version
Availability: from All Versions

## Category
* [Classes](../Categories/Classes.md)
