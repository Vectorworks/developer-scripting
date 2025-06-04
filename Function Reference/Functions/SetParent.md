# SetParent

## Description
Removes the object from its current container and places it within the given container. For example, SetParent can be used to put the referenced object into a group, or into a symbol definition, or to change the layer of the referenced object.

```pascal
FUNCTION SetParent(
				obj       : HANDLE;
				container : HANDLE): BOOLEAN;
```

```python
def vs.SetParent(obj, container):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to the object to move.|
|container|HANDLE|Handle to the object that will become the parent of the obj variable.|

## Remarks
This function will fail if obj is being moved from a non-regenerable list of a plug-in to a regenrable list of a plug-in

SetParent cannot be used for placing a symbol definition in a symbol folder or for bringing it to the document level:

<code lang="pas">
symH := getObject('Decor. 3'); { a symbol definition at top level }
foldH := getObject('Fassade'); { a symbol folder }
temp_b := SetParent(symH, foldH);
alrtDialog(concat(getType(getParent(symH)))); { returns the original parent type 54 (symbol list): setParent didn't work }
</code>

Starting with 12.5, SetParent no longer works within plug-in objects if you're trying to move something from outside of the PIO group into the PIO group. For example, if your PIO requires that you copy geometry out of a symbol definition, and then make some sort of change to it, in previous release, you would typically do something like:

<code lang="pas">
dupeHandle := HDuplicate(somethingInsideSymbol);
SetParent(dupeHandle, pioHandle);
</code>

This no longer works. To accomplish the same purpose, do this:

<code lang="pas">
dupeHandle := CreateDuplicateObject(somethingInsideSymbol, pioHandle);
</code>

This duplicates the object and puts it into the PIO container in one shot.

## Examples
#### VectorScript ####
```pascal
PROCEDURE SetParentExample;
VAR
h1, h2 :HANDLE;
boo :BOOLEAN;
BEGIN
h1 := FSActLayer;
h2 := NextObj(h1);
boo := SetParent(h2, h1);
END;
RUN(SetParentExample);
```
#### Python ####
```python

```

## See Also
VS Functions:
[CreateDuplicateObject](CreateDuplicateObject.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
