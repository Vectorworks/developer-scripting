# SetCustomObjectPath

## Description
Replaces the path of an existing path plug-in object.  The path is used as-is; no translation of vertices is performed.

```pascal
FUNCTION SetCustomObjectPath(
				objectHand : HANDLE;
				path       : HANDLE): BOOLEAN;
```

```python
def vs.SetCustomObjectPath(objectHand, path):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHand|HANDLE|Handle to object.|
|path|HANDLE|Handle to new path polygon.|

## Remarks
This can be used even in non-path objects, where the user is not given any interface for editing the path.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
dialog1  :INTEGER;
objName  :STRING;
objHand  :HANDLE;
pathHand :HANDLE;
boo      :BOOLEAN;
int      :INTEGER;

PROCEDURE dialog1_Setup;
BEGIN
dialog1 := CreateLayout('Pick Object to Create', FALSE, 'OK', 'Cancel');
CreatePulldownMenu(dialog1, 4, 28);
SetFirstLayoutItem(dialog1, 4);
END;

PROCEDURE dialog1_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
CASE item OF
SetupDialogC:
BEGIN
InsertChoice(4, 0, 'Ceiling Grid');
InsertChoice(4, 1, 'Space');
InsertChoice(4, 2, 'Piping Run');
END;
1: GetSelChoice(4, 0, int, objName);
END;
END;

BEGIN
pathHand := FSActLayer;
dialog1_Setup;
IF RunLayoutDialog(dialog1, dialog1_Handler) = 1 THEN BEGIN
objHand := CreateCustomObjectN(objName, 0, 0, 0, FALSE);
boo := SetCustomObjectPath(objHand, pathHand);
END;
END;
RUN(Example);
```
#### Python ####
```python

```

## See Also
VS Functions:
[GetCustomObjectPath](GetCustomObjectPath.md)

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
