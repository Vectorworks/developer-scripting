# BeginContext

## Description
Use this function in conjuction with [EndContext](EndContext.md) to starts logging changes that are made until the EndContext is reached.

```pascal
PROCEDURE BeginContext;
```

```python
def vs.BeginContext():
    return None
```

## Remarks
Use this to begin a logical block of code that creates construct geometry that you intend to delete yourself, and which you don't need to be added to the undo list. For example, if creating a temp symbol for use in a symbol display control, use this so VW won't bog down adding all of the symbol geometry to the undo list.

*\_c\_* (2010.02.10): Begin/EndContext(0) doesn't terminate well if you create hatch definitions. These resources create nevertheless, only their name is removed from the name list. You end up with a nameless resource, even if you delete it before exiting with EndContext(0). (tested VW13 thru 15)

*\_c\_* (2009.05.25): Begin/EndContext don't deal with colors created during the script, for example through PenFore(r, g, b). Even if you terminate the call with EndContext(0) the created colors are there. Actually color creation cannot be undone at all, both as user as well as scripter. (VW 13, 14).

*\_c\_* (2009.04.05): Begin/EndContext must be used in the same procedure block, otherwise they don't work. You can't begin context in a procedure/function and end it somewhere else. This is valid for Commands at least.

*\_c\_* (2008.11.03): This causes troubles to the undo list if you use it through AppleScript in VW 2009. You shouldn't use it through AS until this is fixed.

(unsigned:) If you do not use this construct and you create a temporary plug-in object that itself creates a new class, the new class will remain even after you delete the temporary plug-in object.

## See Also
VS Functions:
[EndContext](EndContext.md)

## Version
Availability: from VectorWorks 12.5

## Category
* [Utility](../Categories/Utility.md)
