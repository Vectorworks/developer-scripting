# ShowGradientEditorDialog

## Description
Displays the gradient editor dialog for the specified gradient. 

To create and edit a new gradient resource, pass in a handle variable initialized to nil. If successful, the handle variable will be initialized with the handle to the new gradient resource.

```pascal
PROCEDURE ShowGradientEditorDialog(VAR gradient : HANDLE);
```

```python
def vs.ShowGradientEditorDialog(gradient):
    return gradient
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|The gradient resource to display in the editor dialog; nil if a new gradient is to be created.|

## Examples
#### VectorScript ####
```pascal
ShowGradientEditorDialog(gradientHandle);
{ displays the specified gradient resource in the editor }

newGradientHandle := nil;
ShowGradientEditorDialog(newGradientHandle);
{ creates a new gradient resource and displays it in the editor }
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
