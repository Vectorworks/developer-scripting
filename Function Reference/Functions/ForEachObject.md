# ForEachObject

## Description
Calls a user defined procedure to operate on each object matching the specified search criteria. 

The procedure subroutine specified by the callback parameter must have one parameter of type HANDLE, which is passed the handle to an object by the ForEachObject call.

```pascal
PROCEDURE ForEachObject(
				callback : PROCEDURE;
				c        : CRITERIA);
```

```python
def vs.ForEachObject(callback, c):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|callback|PROCEDURE|Name of action procedure to be applied to matching objects|
|c|CRITERIA|Search criteria for locating objects.|

## Remarks
*_c_* (2016.05.14): Pay attention how you place your brakets while using criteria strings through variables. Extra brakets might not work and never return errors:
<code lang="pas">
recordName := 'Part Info'; { needs single quotes because of the space }
criteria = Concat('((R in [', '''', recordName, '''', ']))'); { wrap in single quotes }
ForEachObject(ProcThatTakesAHandle, criteria);  { works fine }
ForEachObject(ProcThatTakesAHandle, (criteria));  { doesn't work }
</code>



(Others)
Don't use DelObject inside a ForEachObject callback.

Essentially, ForEachObject is roughly equivalent to
<code lang="pas">
h := FObject;
WHILE h &lt;&gt; NIL DO BEGIN
{do something}
h := NextObj(h);
END;
</code>

The only difference is that ForEachObject is handling the looping for you, and providing a convenient mechanism for filtering the objects by criteria.

Now, if you're deleting h inside that loop, the NextObj call is going to fail miserably. Doing anything that will alter the sequence of entities in the drawing list, inside a loop that walks the drawing list, will produce unexpected results. This includes creating objects, deleting objects, changing the layer of an object, or changing the stacking order ([HMoveForward](HMoveForward.md), [HMoveBackward](HMoveBackward.md)). This will be true if you are walking the drawing list explicitly (using NextObj), or implicitly (using [ForEachObject](ForEachObject.md), [ForEachObjectInLayer](ForEachObjectInLayer.md), or [ForEachObjectInList](ForEachObjectInList.md)).

So use ForEachObject just to build a handle array. Then go back and iterate through the handles, and delete the ones you don't like.

[[User:Rgm|Rgm]] [2012.11.21]:
Note that you can pass in a string for the c:CRITERIA parameter. This appears to be the best way to use variable criteria, e.g.:

<code lang="pas">
recordName := 'Part Info'; { literal, or maybe the value of a function }
criteria = Concat('((R in [', '''', recordName, '''', ']))'); { '''' gives a single quote when parsed }
ForEachObject(ProcThatTakesAHandle, criteria); 
</code>

## Examples
```pascal
PROCEDURE PickRect;

    PROCEDURE SelectThem(h :HANDLE);
    BEGIN
        SetSelect(h);
    END;

BEGIN
   ForEachObject(SelectThem, "T=RECT");
END;
RUN(PickRect);
```
Python:
```python
import vs

def SelectThem(h):
	vs.AlrtDialog( "we're in" + str(h))

vs.AlrtDialog( 'should show three consecutive dialogs' )
vs.ForEachObject( SelectThem, "T=WALL" )
```

## Version
Availability: from All Versions

## Category
* [Criteria](../Categories/Criteria.md)
