# CreateDuplicateObject

## Description
Duplicates the specified object and inserts the new  object into the container.  If container is nil, the new object will be inserted in the active container.

```pascal
FUNCTION CreateDuplicateObject(
				objectToDuplicate : HANDLE;
				containerHandle   : HANDLE): HANDLE;
```

```python
def vs.CreateDuplicateObject(objectToDuplicate, containerHandle):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectToDuplicate|HANDLE|The object to be duplicated|
|containerHandle|HANDLE|The container to the newly duplicated object|

## Remarks
(*_c_*, 2010.10.03): if you are using this call in VW 2011 for copying the poly out of the path group in a path PIO be aware that
* if the PIO instance is showing a 2D surface geometry as "layer" (not "screen") AND
* if the PIO is event enabled and surface eligible (SetObjPropVS(kObjXIs2DSurfEligible, TRUE) AND
* the user modifies the path using the Clip tool
the poly will disappear from display or shift until further regen of the PIO. Until this bug is fixed you can either avoid using this routine (recycling a "PolyCopy" routine) or coerce a regen of the PIO instance using [ResetObject](ResetObject.md)(myPioHandle). This is peculiar of VW 2011 SP1.

(*_c_*, 2008.10.14): It is advisable to coerce the path of path-PIOs to an empty fill. The PIO path is only visible when edited with the 2D Reshape tool. If the path fill is not empty, on edit it will come to foreground and cover whatever else you draw with your PIO, which is most annoying.

<code lang="pas">
pioPathH := GetCustomObjectPath(PioH);
SetFPat(pioPathH, 0); { no fill, otherwise it covers everything up on edit }

pioPathH := CreateDuplicateObject(pioPathH, NIL);
{ make a copy of the path for your further usage
and swap the handle. You don't need the original path any longer.
This copy can have any fill you please }
</code>


(*_c_*, 2009.06.02): This call can be used to duplicate resources, not only objects, but pay great attention to the target container. For example creating in ActLayer a duplicate of a symbol definition (whose parent container should be SymList, type 54), will indeed succeed and create a nameless symbol definition identical to the previous, even visible on drawing, but unselectable. And with parent ActLayer. This can only break your documents and you should avoid it. 

To duplicate a resource simply pass the parent of the resource as target container AND rename the resource with a valid unique name immediately.

<code lang="pas">
h := GetObject('c'); { where c is a sym def }
temp_h := CreateDuplicateObject(h, GetParent(h));
IF temp_h <> NIL THEN SetName(temp_h, 'c2');
</code>


[Charles Chandler, 2006/10/16]: Sounds like this would work nicely for copying path polys out of the path group and into the top level of the PIO container.

## Version
Availability: from VectorWorks 12.5

## Category
* [Object Editing](../Categories/Object%20Editing.md)
