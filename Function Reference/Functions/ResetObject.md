# ResetObject

## Description
Update the specified object using the current settings and parameter values.  This will reset the bounding box of the object.  If the object is in a wall, then the wall is reset also.  

An object of any type may be passed to this function to have its boundary reset.  The following object types will be reset in a way that is appropriate for each type: Plug-in Object, Symbol Definition, Wall, Roof Container, Bitmap, Picture, Dimension, Extrude, Multiple Extrude, Sweep, Polygon, Polyline, Worksheet.

```pascal
PROCEDURE ResetObject(objectHandle : HANDLE);
```

```python
def vs.ResetObject(objectHandle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to the object to be reset.|

## Remarks
To create inter-related objects, where one object will regenerate another, and vice versa, each of the objects has to have a unique identifier. We have found that the only way to do this reliably under all of the circumstances is to put the unique identifier into the "object name" (using SetName). This is ugly, because then the unique identifier is visible to the user, in the Data pane of the Object Info palette. But this is the only way to uniquely identify an object that won't cause problems if the user copies the object. When an object with a name is copied, VW detects that two objects with the same "object name" would create a name conflict, so VW empties the name of the copy, which is what we want. Now the original still has its name, and anything related to it still points to the correct object, which is important of course. When the copy regenerates, it should check to see if it has a name, and if not, it should create one, so that it can be linked to other objects in future operations. We use CreateUUID to generate the unique object name, because it will produce a guaranteed unique identifier.

To relate two objects, use GetName to get this unique identifier, and put it in one of the PIO fields of the related object. Now set the PIO properties to have reset on move and reset on rotate enabled. Now, if the user moves, rotates, or otherwise triggers a reset of the object, you can do a ForEachObject to find the other object that you need to affect.

If your event model requires that multiple PIO types get reset, there is a gotcha. First, VectorScript doesn't do multi-tasking -- it is only capable of running one script at a time. If one object is regenerating, and this object calls ResetObject on another object, the other object will not regenerate until the first script has fully completed. This is usually not such a big problem -- it's just something that you have to know, because there are some things that you cannot do, like reset another object and then check its bounding box for differences. Bounding boxes only get changed when the geometry of an object changes, and this won't happen until the object has regenerated, and if you're still within the script of another object, this hasn't happened yet.

But if you have multiple object types that need to be regenerated, you can run into problems. For instance, if you had a jack object, a cable object, and a splitter object, now you have three different PIO types. So you decide that regenerating the jack object should regenerate the cable object, and this should regenerate the splitter object, and it might have to regenerate another cable object connected to it, and this might need to regenerate another jack object at the far end of the connection. The first jack will successfully regenerate the cable, which will successfully regenerate the splitter. But the splitter will fail to regenerate the second cable, and the last jack will not get regenerated either. In order to improve performance of object regeneration, the VectorScript interpreter looks for all of the PIOs of a certain type that have been flagged for regeneration (ResetObject sets this flag), and it will regenerate all of them before unloading that PIO code and loading the PIO code for the next PIO type. So it will regenerate all of the jack objects that are flagged for regeneration, and THEN all of the cable objects, and THEN all of the splitter objects, and then the interpreter thinks it's done. If your event model doesn't take this into account, the second cable and the second jack will not get regenerated. To solve this, you have to create a routine which gets included in all of your objects, which is capable of handling the entire sequence of changes that have to be made within the first regeneration, and which will use SetRField to update all of the affected objects, and then reset all of them. So the jack object includes "My Great Event Handler.px", which has a routine called SomethingHappened(whatWasIt :STRING). This routine needs to have all of the smarts to chase the change all of the way through. Then you reset everything, the interpreter does the rest. But you can't depend on the interpreter to leap from one object type to the next and then back again, where the smarts are contained within the individual objects.

The one other thing that you have to do is provide a mechanism for preventing an infinite loop in the event model. If every time one of your linked objects gets reset, it runs an event handler which calls SetRField to update its peers, and then calls ResetObject to trigger their regeneration, then you have no exit condition. One way to handle this is to check that the objects need to be reset before resetting them. So your event handler has determined that Object X should have these values in these fields. So do some GetRFields first, to see what's already in those fields, and if they don't need to be changed, don't bother calling SetRField to change them, and don't bother calling ResetObject to regenerate them. Assuming that your event handler has already done all the setting and resetting that needs to be done on the first pass, when the second and successive objects in the chain are regenerating, they will all find that all of the work to all of the other objects has already been done, so no further resets will get triggered. The other way to prevent the infinite loop is to add a field to all of these objects called something like "wasResetByPeer", which should default to false, and which the object should set to false at the end of every execution. Then, when updating a peer object, set this to true. In the code of that object, if it's true, don't enter into the peer-to-peer code block, because you know you don't have to. This way is faster, and a bit more reliable.

## Version
Availability: from VectorWorks10.0

## Category
* [Utility](../Categories/Utility.md)
