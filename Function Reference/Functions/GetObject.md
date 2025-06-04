# GetObject

## Description
Function GetObject returns a handle to a named object. If the name does not exist, NIL is returned.

```pascal
FUNCTION GetObject(name : STRING): HANDLE;
```

```python
def vs.GetObject(name):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|Object name.|

## Remarks
([[User:CBM-c-_| _c_]] 2008.03.26): Quoting Charles two years ago (comment below): "....in case the behavior of GetObject is ever changed to return only results from the main name list...". Today it is the opposite: GetObject will first parse the [[VS:NameList| NameList]] and only if it doesn't find anything there, it will parse the LayerList. 

Back to Charles' example, having a class and a layer with the same name, GetObject will always find the class.

<code lang="pas">
GetObject('xxx') { only a class called "xxx" is present > returns the class }
GetObject('xxx') { only a layer called "xxx" is present > returns the layer }
GetObject('xxx') { both a class and a layer called "xxx" are present > returns the class! }
</code>

(Charles Chandler, 2006.12.7): If there is a layer and also something else (such as a class, viewport, symbol, etc.) in the document with the same name, GetObject will find the layer, and there is no way to force GetObject to see past the layer to return the handle to the other like-named object. The function below can be used to get around this. If you actually want the handle to a layer, you should probably use GetLayerByName instead of GetObject, in case the behavior of GetObject is ever changed to return only results from the main name list.

<code lang="pas">
FUNCTION GetObjectByName(nameOfObject :STRING) :HANDLE;
{Returns the handle to an object in the name list.}
VAR
    h1, h2 :HANDLE;
    tmpName :STRING;
BEGIN
    h1 := GetObject(nameOfObject);
    IF h1 <> NIL THEN BEGIN
        IF GetType(h1) = 31 THEN BEGIN
            {It's a layer, so temporarily rename it, and try again.}
            h2 := h1;
            tmpName := nameOfObject;
            WHILE GetObject(tmpName) <> NIL DO 
                tmpName := Concat('tmp', tmpName);

            SetName(h2, tmpName);
            h1 := GetObject(nameOfObject);
            SetName(h2, nameOfObject);
        END;
    END;
    GetObjectByName := h1;
END;
</code>

## Version
Availability: from All Versions

## Category
* [Object Names](../Categories/Object%20Names.md)
