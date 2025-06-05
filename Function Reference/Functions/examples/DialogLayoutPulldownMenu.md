## VectorScript

```pascal
PROCEDURE AddChoiceSample;
CONST

    { control IDs}
    kCreatePullDownMenu                  = 33;

    kCreatePullDownMenuGroupBox          = 34;

    kCreateListBox                       = 29;
    kCreateListBoxN                      = 30;

    kCreatePushButton                    = 100;

VAR
    dialog            :INTEGER;

PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
    CASE item OF
        SetupDialogC: BEGIN
        
            AddChoice( dialog, kCreatePullDownMenu, 'kCreatePullDownMenu choice', 0 );

            AddChoice( dialog, kCreatePullDownMenuGroupBox, 'kCreatePullDownMenuGroupBox choice', 0 );

            AddChoice( dialog, kCreateListBox, 'kCreateListBox choice', 0 );
            AddChoice( dialog, kCreateListBoxN, 'kCreateListBoxN choice', 0 );

        END;
    END;
END;


BEGIN
    dialog := CreateLayout( 'Add Choice Sample', TRUE, 'OK', 'Cancel' );

    {create controls}

    CreatePullDownMenu( dialog, kCreatePullDownMenu, 24 );

    CreatePullDownMenuGroupBox( dialog, kCreatePullDownMenuGroupBox, 24, 'pull down menu', TRUE );

    CreatePushButton( dialog, kCreatePushButton, 'push button' );
    SetFirstGroupItem( dialog, kCreatePullDownMenuGroupBox, kCreatePushButton );

    CreateListBox( dialog, kCreateListBox, 24, 4 );
    CreateListBoxN( dialog, kCreateListBoxN, 24, 4, TRUE );


    {set relations}
    SetFirstLayoutItem( dialog, kCreatePullDownMenu );
 
    SetBelowItem( dialog, kCreatePullDownMenu, kCreatePullDownMenuGroupBox, 0, 0 );

    SetBelowItem( dialog, kCreatePullDownMenuGroupBox, kCreateListBox, 0, 0 );
    SetBelowItem( dialog, kCreateListBox, kCreateListBoxN, 0, 0 );



    IF RunLayoutDialog( dialog, Dialog_Handler ) = 1 then BEGIN
    END;

END;
RUN( AddChoiceSample );
```

## Python

```python
def AddChoiceSample():
	# control IDs
	global kCreatePullDownMenu                
	global kCreatePullDownMenuGroupBox 
	global kCreateListBox                          
	global kCreateListBoxN                        
	global kCreatePushButton   
	global SetupDialogC
	kCreatePullDownMenu                = 33
	kCreatePullDownMenuGroupBox = 34
	kCreateListBox                          = 29
	kCreateListBoxN                        = 30
	kCreatePushButton                    = 100
	SetupDialogC = 12255


def Dialog_Handler(item, data):
	if (item == SetupDialogC):
		vs.AddChoice( dialog, kCreatePullDownMenu, 'kCreatePullDownMenu choice', 0 )
		vs.AddChoice( dialog, kCreatePullDownMenuGroupBox, 'kCreatePullDownMenuGroupBox choice', 0 )
		vs.AddChoice( dialog, kCreateListBox, 'kCreateListBox choice', 0 )
		vs.AddChoice( dialog, kCreateListBoxN, 'kCreateListBoxN choice', 0 )

def CreateMyDialog():
	global dialog
	dialog = vs.CreateLayout( 'Add Choice Sample', 1, 'OK', 'Cancel' )

	#{create controls}

	vs.CreatePullDownMenu( dialog, kCreatePullDownMenu, 24 )

	vs.CreatePullDownMenuGroupBox( dialog, kCreatePullDownMenuGroupBox, 24, 'pull down menu', 1 )

	vs.CreatePushButton( dialog, kCreatePushButton, 'push button' )
	vs.SetFirstGroupItem( dialog, kCreatePullDownMenuGroupBox, kCreatePushButton )

	vs.CreateListBox( dialog, kCreateListBox, 24, 4 )
	vs.CreateListBoxN( dialog, kCreateListBoxN, 24, 4, 1 )


	#{set relations}
	vs.SetFirstLayoutItem( dialog, kCreatePullDownMenu )
 
	vs.SetBelowItem( dialog, kCreatePullDownMenu, kCreatePullDownMenuGroupBox, 0, 0 )

	vs.SetBelowItem( dialog, kCreatePullDownMenuGroupBox, kCreateListBox, 0, 0 )
	vs.SetBelowItem( dialog, kCreateListBox, kCreateListBoxN, 0, 0 )

	if vs.RunLayoutDialog( dialog, Dialog_Handler ) == 1:
		pass

kCreatePullDownMenu = 0               
kCreatePullDownMenuGroupBox  = 0 
kCreateListBox     = 0                       
kCreateListBoxN    = 0                      
kCreatePushButton    = 0 
SetupDialogC = 0 
dialog = 0
AddChoiceSample()
CreateMyDialog()
```
