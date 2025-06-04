# CreateCustomObjectPath

## Description
Creates an instance of the path custom object specified by the name argument.  The vertices of the path are translated in such a way that the first vertex will be placed at the origin of the plug-in's coordinate space.

```pascal
FUNCTION CreateCustomObjectPath(
				objectName   : STRING;
				path         : HANDLE;
				profileGroup : HANDLE): HANDLE;
```

```python
def vs.CreateCustomObjectPath(objectName, path, profileGroup):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|Name of object.|
|path|HANDLE|Handle to new object path polygon.|
|profileGroup|HANDLE|Handle to new profile group object.|

## Remarks
Calls DefineCustomObject() first to either find the defining FormatNode or create it.  If it is created, the user will be presented with an initialization dialog.  Returns handle to Object.

If the path object code creates a symbol (BeginSym~EndSym), the page center gets messed up, and the only way to fix it is to manually enter and then exit a group or sym def, or to use the previous view button and then the fit to page button. This has been entered as a bug -- I'll remove this comment when the bug is fixed.

It is nothing new, but this routine will create a custom object instance that doesn't resolve as "New Object". If inside the Plug-in code you are using IsNewCustomObject(pioName) you'd expect the object just created to be recognized as new. But IsNewCustomObject will never return TRUE on objects created by CreateCustomObjectPath.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
h :HANDLE;
BEGIN
CallTool(-204);
h := CreateCustomObjectPath('Cutting Plane', FSActLayer, nil);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	vs.CallTool(-204)
	vs.CreateCustomObjectPath('Cutting Plane', vs.FSActLayer(), None)
Example()
```

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
