# RegisterDialogForTimerEvents

## Description
Register the dialog so that it can receive events periodically using the given time delay.

```pascal
PROCEDURE RegisterDialogForTimerEvents(
				dialogID                 : LONGINT;
				timerDelayInMilliseconds : LONGINT);
```

```python
def vs.RegisterDialogForTimerEvents(dialogID, timerDelayInMilliseconds):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the dialog identifier given by CreateLayout or CreateResizableLayout|
|timerDelayInMilliseconds|LONGINT|The amount of time in milliseconds between each sent each DialogTimerEventMessageC.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR

    dialog1         :INTEGER;
    result          :INTEGER;
    switch          :INTEGER;

    PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
    BEGIN
        CASE item OF
            SetupDialogC:
            BEGIN
    
                RegisterDialogForTimerEvents( dialog1, 500 );

            END;

            4:
            BEGIN
                RegisterDialogForTimerEvents( dialog1, 500 );
                SetControlText( dialog1, 6, 'registered' );
            END;

            5:
            BEGIN
                DeregisterDialogFromTimerEvents( dialog1 );
                SetControlText( dialog1, 6, 'deregistered' );
            END;

            DialogTimerEventMessageC:
            BEGIN
                IF ( switch = 1 ) THEN
                    SetControlText( dialog1, 6, 'First' )
                ELSE
                    SetControlText( dialog1, 6, 'Second' );

                IF ( switch = 1 ) THEN
                    switch := 2
                ELSE
                    switch := 1;
                
            END;

        END;

    END;

BEGIN

    switch  := 1;

    dialog1 := CreateLayout( 'Create Control - Gradient Slider', FALSE, 'OK', 'Cancel' );

    CreatePushButton( dialog1, 4, 'Register');
    CreatePushButton( dialog1, 5, 'UnRegister');
    CreateStaticText( dialog1, 6, 'hello', 20 );
    
    SetFirstLayoutItem( dialog1, 4 );
    SetBelowItem( dialog1, 4, 5, 0, 0 );
    SetBelowItem( dialog1, 5, 6, 0, 0 );

    result := RunLayoutDialog(dialog1, Dialog_Handler);

END;

RUN(Example);
```
#### Python ####
```python

```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
