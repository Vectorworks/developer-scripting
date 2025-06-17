# Object Events

How to enable the extended plug-in properties and handle script specified events. Article by Charles Chandler, from the former Vectorlab, 2007.

## Object Events

All VectorScript objects respond to the following events:

### Icon Single-Click

This event is triggered when the user clicks on the object's icon in the tool palette.

At this time, VW checks to see if there is a **name conflict** between the object and anything else already in the drawing. If there is a worksheet, or saved view, or anything else in the name list that has the same name, but is not a plug-in object, VW aborts the activation of the tool. There is no way to check for this within the object code, and VW does not inform the user of the nature of the problem. So make sure your object names are not going to conflict with anything else in the drawing.

If there is not a name conflict, the object type is read, to determine what options should be put in the Mode bar. This varies depending on the type of object (point, line, rectangle, etc.).

If it's a **point object**, the object code is run, to generate the preview geometry that will follow the cursor around until the object is placed, to help the user visualize the size and shape of the object before placement. If `GetPref(531)` returns `true`, the object code was triggered by this event, and you may want to do some things differently in this case, such as by-pass complex geometry which is not necessary for the preview and which slows down the placement process too much.

### Icon Double-Click

This event is triggered when the user **double-clicks** on the object's icon in the tool palette.

The Create Object dialog is displayed, allowing the user to specify the default object properties, and then an object with those values is created in the document.

### Object Creation

* Object was created by clicking the object's icon in the tool palette, and then clicking in the drawing, or by double-clicking the icon and entering the desired values.
* Object was cut or copied, and then pasted into the drawing.
* Object (in red symbol form) was inserted into the drawing from the Resource Browser.
* Object was created by another script, using `VS:CreateCustomObject`, `VS:CreateCustomObjectN`, or `VS:ImportResourceToCurrentFile`/ `VS:CopySymbol` (and the symbol is a red symbol).

### Existing Object Reset

* **Parameters** were changed in the Object Info palette.
* The **object's script** was edited, using the VectorScript Plug-in Editor.
* Attributes of the object's **class**, or of a class used somewhere inside the object, were changed.
* **Another script** (object or menu command) called ResetObject to trigger a regeneration of the object.
* Object was **rotated**, and Reset on Rotate was set in the plug-in editor.
* Object was **moved**, either from one location to another in the same layer, or from one layer to another, and Reset on Move was set in the plug-in editor.

## Extended Properties

Using the Extended Properties features, more behaviors are available to VectorScript objects.

Before you start using these advanced features, you should understand that PIOs that use them are three times more complicated than PIOs that do not. The nice thing about "regular" VectorScript objects is that you can get decent results with a minimum of effort. You may not be able to get exactly the behaviors that you want, but what you do get, you get easily.

When you start working with the new extended properties of VectorScript objects, you get to do things which you could not do before, but you have to do a LOT more work to do them. With increased power and flexibility comes increased complexity and risk. Managing the complexity, in an environment that lets you cause problems that you couldn't cause before, substantially increases the development effort. And in many cases, you may find that the VectorScript environment is still too limiting, and that you really ought to be developing the features in C++, where you will have virtually unlimited power and flexibility, and will never have to re-design a feature because of something you couldn't do in VectorScript, or spend enormous amounts of time trying to find ways around its limitations.

The **C++ environment** is more complicated than VectorScript, but not as complicated as trying to get a limited language like VectorScript to do things for which it was not designed. Besides, these new features in VectorScript were implemented not in an effort to make VectorScript objects as powerful and flexible as SDK objects, but simply to satisfy very specific requirements for specific features under development at NNA. The general public is encouraged to use these features at their own risk, and to not expect the functionality to be rounded out in future releases, the way core functionality is maintained, enhanced, and supported.

That having been said...

### Enable Script Specified Events

To **enable** these events or event behavior changes, use the VectorScript Plug-in Editor to set the **With Script-Specified Events** property in the Properties dialog.

If you want the object to respond to *script-specified* events as well as rotate and/or move:

* in the plug-in editor, set the script execution to **Reset Only**,
* then check the Reset on Rotate and/or **Reset on Move** boxes,
* **re-check** the **With Script-Specified Events** box again.

The *Reset* on *Rotate/Move* values will still be valid, even though they appear as disabled options in the dialog.

Events that can be added or modified include:

### Mode Bar Behaviors

#### Preferences Button

If an object's icon is clicked in the tool palette, a *Preferences* button will appear in the Mode bar. By default, if the user clicks this button, the **VectorWorks - Object Properties** dialog is displayed, which allows the user to specify the default values for future instances of the object in that drawing. Clicking this button can, instead, pop up a custom dialog created by the developer.

The Door object is an example of a PIO that uses a custom dialog for the Preferences event.

The Preferences event is also raised when the **first instance** of an object is created in a new document, so a custom preferences dialog must successfully handle this case as well.

See [Example 1](#example-1).

#### Wall Insertion Mode

PIOs by default can be inserted into walls on creation, if the Wall Insertion Mode button in the Mode bar is active. This can be suppressed, if you know that the PIO should never be inserted into walls.

See [Example 2](#example-2).

### Object Info Palette Behaviors

By default, when an object is initialized, all of its parameters are loaded into the Object Info palette. Then the code is run, to see if any `VS:SetParameterVisibility` or `VS:EnableParameter` calls are made, and the Object Info palette is reset to accommodate any changes that were made by those calls. There is one additional element which can be added to the Object Info palette -- a button which will raise an event. Typically this is used to display a dialog which allows the user to specify things which would be difficult or impossible to specify on the Object Info palette.

See [Example 3](#example-3).

Path objects by default have polyline editing controls on the Object Info palette. These can be suppressed.

See [Example 4](#example-4).

### Layer Scale Change

Some objects have to be regenerated after a change is made to the layer scale in order to display properly. Typically these are objects which create text. Enable this property to get layer scale changes to trigger the regeneration of a custom PIO.

See [Example 5](#example-5).

### Edit Group

Path objects respond to the Edit Group command. By default, the **Choose Component** dialog is displayed, allowing the user to select either the path or the profile to edit. If one or the other of these options is not relevant, there is no need to offer this choice to the user. In this case, the *Choose Component* dialog can be by-passed, and the user can be sent directly into the appropriate editing mode.

See [Example 6](#example-6).

### Add/Intersect/Clip Surface

By default, path objects do not respond to **surface operations**. Set this property to allow users to edit custom path objects with surface operations.

See [Example 7](#example-7).

### Marker

By default, line and path objects do not respond to **marker properties** set using the Attributes palette. Set this property to allow users to apply markers using the Attributes palette.

See [Example 8](#example-8).

### Edit Object

By default, if the user invokes the **Edit...** command with a PIO selected, or double-clicks on a PIO instance, a dialog saying *"The selected object has no edit behavior."* is displayed. If this property is enabled, one of four behaviors can be specified for this event.

See [Example 9](#example-9).

The default edit behavior can be invoked. For **path objects**, this is the *Edit Group* behavior. For **other object types**, the dialog saying *"The selected object has no edit behavior."* will be displayed.

A custom edit behavior can be defined. In this case, the edit action will raise the **kObjXPropSpecialEdit** event, which can be handled in the object's event loop. Typically this is used to display a dialog into which the user can enter parameter values, and which would typically be the same dialog the user sees in the Preferences event.

The VW Properties dialog can be displayed. No VectorScript event is raised for this.

For path objects, the 2D Reshape tool can be activated.

### A Note on Creating Geometry and/or Text *Inside* versus *Outside* of the PIO

In "regular" PIOs, any VW primitive (geometry or text) that you create will become a member of the PIO. If the PIO is moved, the primitive will move along with it. If the PIO is deleted, the primitive will be deleted as well. This is still true of any primitives that you create within the reset event of an extended properties PIO. But it is not true of primitives created during any of the other events. For example, if you create a rectangle during the button click event of an extended properties PIO, that rectangle will be created in the document coordinate system, not within the local coordinate system of the PIO, and it will not be a member of the PIO. If the user deletes the PIO, the rectangle will remain. So any primitives that you intend to be a member of the PIO can only be created within the reset case of the event loop.

See [Example 10](#example-10).

## Examples

### Example 1

Object with a custom preference dialog:

```pascal
PROCEDURE Example1;
CONST
    kObjOnInitXProperties = 5;
    kObjXPropPreference = 4;
    kOnObjPrefEventID = 4;
    kResetEventID = 3;
VAR
    theEvent, theButton :LONGINT;
    result :BOOLEAN;
BEGIN
    vsoGetEventInfo(theEvent, theButton);
    CASE theEvent OF

        {User has single-clicked the object's icon.}
        kObjOnInitXProperties: 
            BEGIN
                {This tells VW to pass the preference event back
                to this object, as the kOnObjPrefEventID event,
                instead of calling the built-in preference handler,
                which pops up the Object Properties dialog.}
                result := SetObjPropVS(kObjXPropPreference, TRUE);
            END;

        {User has clicked the Preferences button in the Mode bar, or
        double-clicked the object in the drawing (see example 9). This
        event will never happen if the kObjXPropPreference property is
        not set to TRUE in the initialization event (above).}
        kOnObjPrefEventID: 
            BEGIN
                {Typically this dialog accepts user input and uses SetRField
                to write the values to the object's record definition handle.}
                AlrtDialog('Custom Preference Dialog');
            END;

        {Object reset has been called.}
        kResetEventID: 
            BEGIN
                Rect(0, 0, 1, 1);
            END;

    END;
END;
RUN(Example1);
```

### Example 2

Object that won't go into a wall:

```pascal
PROCEDURE Example2;
CONST
    kObjOnInitXProperties = 5;
    kResetEventID = 3;
    kObjXPropPreventWallInsertion = 7;
VAR
    theEvent, theButton :LONGINT;
    result :BOOLEAN;
BEGIN
    vsoGetEventInfo(theEvent, theButton);
    CASE theEvent OF

        {User has single-clicked the object's icon.}
        kObjOnInitXProperties: 
            BEGIN
                {This tells VW to abort the creation of a new instance
                of the object if the user has clicked on top of a wall.}
                result := SetObjPropVS(kObjXPropPreventWallInsertion, TRUE);
            END;

        {Object reset has been called.}
        kResetEventID: 
            BEGIN
                Rect(0, 0, 1, 1);
            END;

    END;
END;
RUN(Example2);
```

### Example 3

Object that has a button on the Object Info palette:

```pascal
PROCEDURE Example3;
CONST
    kObjOnInitXProperties = 5;
    kResetEventID = 3;
    kObjXPropHasUIOverride = 8;
    kWidgetButton = 12;
    kObjOnObjectUIButtonHit = 35;
    buttonID_1 = 1234; {user-definable index}
VAR
    theEvent, theButton :LONGINT;
    result :BOOLEAN;
    sourceFieldNumber :INTEGER;
    buttonEventID :INTEGER;
    displayString :STRING;
    thisDoesNothing :LONGINT;
BEGIN
    vsoGetEventInfo(theEvent, theButton);
    CASE theEvent OF

        {User has single-clicked the object's icon.}
        kObjOnInitXProperties: 
            BEGIN
                {This tells VW to let the object decide what goes
                onto the Object Info palette.}
                result := SetObjPropVS(kObjXPropHasUIOverride, TRUE);

                {Now we manually add the "normal" parameters...}

                {One way is to use this single call to add all
                of the existing parameters.}
                result := vsoInsertAllParams;

                {Alternatively, you can use this to tack individual parameters 
                onto the end of the list one at a time. This way, you don't have 
                to use SetParameterVisibility in the reset event to hide parameters
                that you never want to see.}
                sourceFieldNumber := 1;
                displayString := 'My Great Field Name';
                result := vsoAppendParamWidget(sourceFieldNumber, displayString, thisDoesNothing);

                {Finally, we add the button.}
                displayString := 'My Great Button';
                result := vsoAppendWidget(kWidgetButton, buttonID_1, displayString, thisDoesNothing);
            END;

        {User has clicked a button in the Object Info palette.}
        kObjOnObjectUIButtonHit:
            BEGIN
                CASE theButton OF
                    buttonID_1:
                        BEGIN
                            AlrtDialog('Custom Button Dialog');
                        END;
                END;
            END;

        {Object reset has been called.}
        kResetEventID: 
            BEGIN
                Rect(0, 0, 1, 1);
            END;

    END;
END;
RUN(Example3);
```

### Example 4

Path object without vertex editing controls or 3D location widget on the Object Info palette:

```pascal
PROCEDURE Example4;
CONST
    kObjOnInitXProperties = 5;
    kResetEventID = 3;
    kObjXPropDefaultPropertyUI = 11;
    kObjXPropHide3DLocationWidget = 1;
    kHidePolyWidget = 2;
VAR
    theEvent, theButton :LONGINT;
    result :BOOLEAN;
    objHand, recHand, wallHand, pathHand, dupeHand :HANDLE;
    objName :STRING;
BEGIN
    vsoGetEventInfo(theEvent, theButton);
    CASE theEvent OF

        {User has single-clicked the object's icon.}
        kObjOnInitXProperties: 
            BEGIN
                {This tells VW to suppress the vertex editing controls 
                and the 3D location widget on the Object Info palette.}
                result := SetObjPropCharVS(kObjXPropDefaultPropertyUI, Chr(kObjXPropHide3DLocationWidget));
                result := SetObjPropCharVS(kObjXPropDefaultPropertyUI, Chr(kHidePolyWidget));
            END;

        {Object reset has been called.}
        kResetEventID: 
            BEGIN
                IF GetCustomObjectInfo(objName, objHand, recHand, wallHand) THEN BEGIN
                    pathHand := GetCustomObjectPath(objHand);
                    dupeHand := CreateDuplicateObject(pathHand, objHand);
                END;
            END;

    END;
END;
RUN(Example4);
```

### Example 5

Object that gets reset if the layer scale changes:

```pascal
PROCEDURE Example5;
CONST
    kObjOnInitXProperties = 5;
    kResetEventID = 3;
    kObjXPropHasLayerScaleDeps = 2;
VAR
    theEvent, theButton :LONGINT;
    result :BOOLEAN;
BEGIN
    vsoGetEventInfo(theEvent, theButton);
    CASE theEvent OF

        {User has single-clicked the object's icon.}
        kObjOnInitXProperties: 
            BEGIN
                {This tells VW to reset the object if the layer scale changes.}
                result := SetObjPropVS(kObjXPropHasLayerScaleDeps, TRUE);
            END;

        {Object reset has been called.}
        kResetEventID: 
            BEGIN
                Rect(0, 0, 1, 1);
                AlrtDialog('yep, I am regenerating');
            END;

    END;
END;
RUN(Example5);
```

### Example 6

Path object with "edit path" as the Edit Group behavior:

```pascal
PROCEDURE Example6;
CONST
    kObjOnInitXProperties = 5;
    kResetEventID = 3;
    kObjXPropEditGroup = 1;
    kObjXPropEditGroupPath = 2;
    kObjXPropEditGroupProfile = 1;
VAR
    theEvent, theButton :LONGINT;
    result :BOOLEAN;
    objHand, recHand, wallHand, pathHand, dupeHand :HANDLE;
    objName :STRING;
BEGIN
    vsoGetEventInfo(theEvent, theButton);
    CASE theEvent OF

        {User has single-clicked the object's icon.}
        kObjOnInitXProperties: 
            BEGIN
                {This defines the Edit Group behavior to be "path".}
                result := SetObjPropCharVS(kObjXPropEditGroup, Chr(kObjXPropEditGroupPath));
            END;

        {Object reset has been called.}
        kResetEventID: 
            BEGIN
                IF GetCustomObjectInfo(objName, objHand, recHand, wallHand) THEN BEGIN
                    pathHand := GetCustomObjectPath(objHand);
                    dupeHand := CreateDuplicateObject(pathHand, objHand);
                END;
            END;

    END;
END;
RUN(Example6);
```

### Example 7

Path object that responds to surface editing:

```pascal
PROCEDURE Example7;
CONST
    kObjOnInitXProperties = 5;
    kResetEventID = 3;
    kObjXIs2DSurfaceEligible = 14;
VAR
    theEvent, theButton :LONGINT;
    result :BOOLEAN;
    objHand, recHand, wallHand, pathHand, dupeHand :HANDLE;
    objName :STRING;
BEGIN
    vsoGetEventInfo(theEvent, theButton);
    CASE theEvent OF

        {User has single-clicked the object's icon.}
        kObjOnInitXProperties: 
            BEGIN
                {This allows the object to respond to surface editing.}
                result := SetObjPropVS(kObjXIs2DSurfaceEligible, TRUE);
            END;

        {Object reset has been called.}
        kResetEventID: 
            BEGIN
                IF GetCustomObjectInfo(objName, objHand, recHand, wallHand) THEN BEGIN
                    pathHand := GetCustomObjectPath(objHand);
                    dupeHand := CreateDuplicateObject(pathHand, objHand);
                END;
            END;

    END;
END;
RUN(Example7);
```

### Example 8

Path object that accepts markers from the Attributes palette:

```pascal
PROCEDURE Example8;
CONST
    kObjOnInitXProperties = 5;
    kResetEventID = 3;
    kObjXPropAcceptsMarkers = 10;
    kObjXPropAcceptsNoneMarkers = 0;
    kObjXPropAcceptsBeginningOnlyMarkers = 1;
    kObjXPropAcceptsEndOnlyMarkers = 2;
    kObjXPropAcceptsBothMarkers = 3;
VAR
    theEvent, theButton :LONGINT;
    result :BOOLEAN;
    objHand, recHand, wallHand, pathHand, dupeHand :HANDLE;
    objName :STRING;
    gArrowIndex :INTEGER;
    gMarkerSize, gMarkerAng :REAL;
    begArr, endArr :BOOLEAN;
BEGIN
    vsoGetEventInfo(theEvent, theButton);
    CASE theEvent OF

        {User has single-clicked the object's icon.}
        kObjOnInitXProperties: 
            BEGIN
                {This allows the object to accept marker setting from the Attributes palette.}
                result := SetObjPropCharVS(kObjXPropAcceptsMarkers, Chr(kObjXPropAcceptsBothMarkers));
            END;

        {Object reset has been called.}
        kResetEventID:
            BEGIN
                IF GetCustomObjectInfo(objName, objHand, recHand, wallHand) THEN BEGIN
                    pathHand := GetCustomObjectPath(objHand);
                    dupeHand := CreateDuplicateObject(pathHand, objHand);

                    {Get the settings from objHand and apply them to dupeHand.}
                    {Note that Get/SetObjArrow are obsolete in 2008.}
                    {Use Get/SetObjBeginningMarker and Get/SetObjEndMarker in 2008 or above.}
                    GetObjArrow(objHand, gArrowIndex, gMarkerSize, gMarkerAng, begArr, endArr);
                    SetObjArrow(dupeHand, gArrowIndex, gMarkerSize / GetPrefReal(152), gMarkerAng, begArr, endArr);
                END;
            END;

    END;
END;
RUN(Example8);
```

### Example 9

Path object that goes into 2D Reshape mode on double-click:

```pascal
PROCEDURE Example9;
CONST
    kObjOnInitXProperties = 5;
    kResetEventID = 3;
    kObjXPropSpecialEdit = 3;
    kDefaultSpecialEdit = 0;
    kCustomSpecialEdit = 1;
    kPropertiesSpecialEdit = 2;
    kReshapeSpecialEdit = 3;
VAR
    theEvent, theButton :LONGINT;
    result :BOOLEAN;
    objHand, recHand, wallHand, pathHand, dupeHand :HANDLE;
    objName :STRING;
BEGIN
    vsoGetEventInfo(theEvent, theButton);
    CASE theEvent OF

        {User has single-clicked the object's icon.}
        kObjOnInitXProperties: 
            BEGIN
                {This defines the double-click behavior to active the 2D Reshape tool.}
                result := SetObjPropCharVS(kObjXPropSpecialEdit, Chr(kReshapeSpecialEdit));
            END;

        {Object reset has been called.}
        kResetEventID:
            BEGIN
                IF GetCustomObjectInfo(objName, objHand, recHand, wallHand) THEN BEGIN
                    pathHand := GetCustomObjectPath(objHand);
                    dupeHand := CreateDuplicateObject(pathHand, objHand);
                END;
            END;

    END;
END;
RUN(Example9);
```

### Example 10

Object that creates geometry in the drawing, not within the PIO:

```pascal
PROCEDURE Example10;
CONST
    kObjOnInitXProperties = 5;
    kResetEventID = 3;
    kObjXPropHasUIOverride = 8;
    kWidgetButton = 12;
    kObjOnObjectUIButtonHit = 35;
    buttonID_1 = 1234; {user-definable index}
VAR
    theEvent, theButton :LONGINT;
    result :BOOLEAN;
    buttonEventID :INTEGER;
    displayString :STRING;
    thisDoesNothing :LONGINT;
BEGIN
    vsoGetEventInfo(theEvent, theButton);
    CASE theEvent OF

        {User has single-clicked the object's icon.}
        kObjOnInitXProperties: 
            BEGIN
                {This tells VW to let the object decide what goes
                onto the Object Info palette.}
                result := SetObjPropVS(kObjXPropHasUIOverride, TRUE);

                {Add the button.}
                displayString := 'Create Stray Rectangle';
                result := vsoAppendWidget(kWidgetButton, buttonID_1, displayString, thisDoesNothing);
            END;

        {User has clicked a button in the Object Info palette.}
        kObjOnObjectUIButtonHit:
            BEGIN
                CASE theButton OF
                    buttonID_1:
                        BEGIN
                            {This rectangle is created OUTSIDE of the PIO.}
                            Rect(0, 0, 1, 1);
                        END;
                END;
            END;

        {Object reset has been called.}
        kResetEventID: 
            BEGIN
                {This rectangle is created INSIDE of the PIO.}
                Rect(0, 0, 1, 1);
            END;

    END;
END;
RUN(Example10);
```