# SetName

## Description
Procedure SetName assigns a name to the referenced object.

```pascal
PROCEDURE SetName(
				h    : HANDLE;
				name : STRING);
```

```python
def vs.SetName(h, name):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|name|STRING|Name to be assigned to object.|

## Remarks
From Tom: as of 950, this can be used to rename layers, despite the fact that its inverse, GetName, fails and generates a VS warning when used on layers. (Use GetLName here instead)



Note that if "name" is already in use by something else in the name list, SetName will fail with the warning, "Name already exists," and the object's previous name will persist. This conflict checking is not case-sensitive. If you need to know whether or not the new name stuck, check the name after setting it:
<code lang="pas">
FUNCTION SetNameSucceeded(h :HANDLE; theNameToSet :STRING) :BOOLEAN;
BEGIN
SetName(h, theNameToSet);
SetNameSucceeded := (GetName(h) = theNameToSet);
END;
</code>

Also note that while GetName will return 'none' for an object which has not been given a name yet, GetObject('none') will either return a nil handle, or it will return the handle to the None class, if such a class exists in the document. If the None class is present, you cannot assign the name "none" to any new object, because of the name conflict. If the None class ''is not'' present, SetName(objectHandle, 'none') will not generate a warning, but you still won't be able to access the object using GetObject. In other words, an object name of "none" is sort of like an empty name, except that it can't be set if there's a None class in the document.

One more thing: _never rename the None class!_ Many things in VW (English edition) expect this to be present, and will access it literally. If you want to initialize object names, do it like this: SetName(objectHandle, ''). Then GetName(objectHandle) will return ''.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
h1    :HANDLE;
SName :STRING;
BEGIN
SName := 'Fred';
h1 := CreateSphere(0, 0, 0, 1000);
SetName(h1, SName);
END;
RUN(Example);
```
#### Python ####
```python
SName = 'Fred'
h1 = vs.CreateSphere(0, 0, 0, 1000)
vs.SetName(h1, SName)
```

## See Also
VS Functions:
[GetName](GetName.md)

## Version
Availability: from All Versions

## Category
* [Object Names](../Categories/Object%20Names.md)
