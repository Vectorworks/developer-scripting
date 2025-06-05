## VectorScript

```pascal
PROCEDURE Test; 
CONST
    ObjectType = 97; { Texture Definition } 
    FolderIndex = 100; { BuildResourceList Def for Texture Folder See Func. Ref } 
    SubFolderName = ''; { Nul subfolder get all folders and subfolders } 

VAR
    MyName : STRING; 
    MyList : LONGINT; 
    NumItems : LONGINT; 
	hatch : HANDLE;

BEGIN
    MyList := BuildResourceList(ObjectType, FolderIndex, '', NumItems); 
    MyName := GetNameFromResourceList(MyList, 1); { change this number to get the names of other textures } 
    Message( Date(2, 2), ': The Name is ', MyName, ' *** Total items in list: ', NumItems); 
	
	hatch := GetResourceFromList(MyList, 1);
	IF (hatch = NIL) THEN
	hatch := ImportResourceToCurrentFile(MyList, 1);
	
	DeleteResourceFromList(MyList, 1);
END; 
RUN(Test);
```

## Python

```python
def Test():
    ObjectType = 97 # Texture Definition
    FolderIndex = 100 # BuildResourceList Def for Texture Folder See Func. Ref
    SubFolderName = '' # Nul subfolder get all folders and subfolders

    MyList, NumItems = vs.BuildResourceList(ObjectType, FolderIndex, '')
    MyName = vs.GetNameFromResourceList(MyList, 1) # change this number to get the names of other textures
    vs.Message( vs.Date(2, 2), ': The Name is ', MyName, ' *** Total items in list: ', NumItems)
	
    hatch = vs.GetResourceFromList(MyList, 1)
    if (hatch == None):
        hatch = vs.ImportResourceToCurrentFile(MyList, 1)
	
    vs.DeleteResourceFromList(MyList, 1)
	
Test()
```
