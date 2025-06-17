By [Vladislav Stanev](mailto:vstanev@nemetschek.net)

## What's that

...

## Parametric Object Part

Your parametric object has to be event enabled.

The parametric object responds to an event with the name of the tool that should be activated.

```vs
BEGIN {MAIN}
  result := GetCustomObjectInfo(objectName, objectHand, recordHand, wallHand);
  vsoGetEventInfo(theEvent, message );

  CASE theEvent OF
    43: {kObjOnGetToolName}
    BEGIN
      vsoSetObjToolName( message, 'SampleTool' );
    END;
```

## Tool Part

The tool plug-in must be event enabled.

The tool is notified by VectorWorks for the object that needs to be duplicated.

```vs
BEGIN {MAIN}
  vstGetEventInfo (eventID, modeGroup, modeButton);
  CASE eventID OF
    116: {kToolInitByObject}
    BEGIN
        hOrgObject := vstGetInitObject( modeGroup );
        {set up the tool by the specified source object
         ...}
    END;