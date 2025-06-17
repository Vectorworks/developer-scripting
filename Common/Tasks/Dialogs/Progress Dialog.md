By [Vladislav Stanev](mailto:vstanev@nemetschek.net)

## VectorScript

### Example 1

Fake work by waiting and using a cancel-able dialog.

```vs
PROCEDURE TestProgressDlg;
VAR
	hasCanceled : BOOLEAN;

	PROCEDURE DoHalfTheWork;
	CONST kWORK = 26;
	VAR i : INTEGER;
	BEGIN
		{we do 50% of the work in kWORK loops/calls to yield}
		ProgressDlgStart( 50.0, kWORK );
		
		i := 1;
		WHILE (i <= kWORK) AND (NOT hasCanceled) DO
		BEGIN
			Wait( 1 ); {well, we work by waiting}
			
			ProgressDlgYield( 1 );
			hasCanceled := ProgressDlgHasCancel;

			i := i + 1;
		END;
		
		ProgressDlgEnd;
	END;
	
BEGIN
	hasCanceled := FALSE;

	ProgressDlgOpen( 'I''m about to do some heavy work', TRUE );
	ProgressDlgSetTopMsg( 'Top message to inform about something' );
	ProgressDlgSetBotMsg( 'Bottom message to force the information in' );
	
	ProgressDlgSetMeter( 'Doing the first half of the work...' );
	DoHalfTheWork;
	
	ProgressDlgSetMeter( 'Doing the SECOND half...' );
	DoHalfTheWork;
	
	ProgressDlgClose;
END;
RUN(TestProgressDlg);
```

### Example 2

Resetting the selected objects with a progress dialog without cancel button.

```vs
PROCEDURE TestProgressDlg;
VAR
	selCount : LONGINT;

	PROCEDURE DoTheWork;
	VAR
		i : LONGINT;
		h : HANDLE;
	BEGIN
		selCount := NumSelectedObjects;

		{we do 90% of the work of resetting selected objects}
		ProgressDlgStart( 90.0, selCount );
		
		h := FSActLayer;
		FOR i := 1 TO selCount DO
		BEGIN
			Wait( 1 ); {well, we work by waiting}

			ResetObject( h );

			h := NextSObj( h );

			ProgressDlgYield( 1 );
		END;
		
		ProgressDlgEnd;
	END;
	
BEGIN
	ProgressDlgOpen( 'I''m about to do some reset work', FALSE );
	
	ProgressDlgSetMeter( 'Resetting objects...' );
	DoTheWork;
		
	ProgressDlgSetMeter( 'Finishing...' );
	ProgressDlgStart( 10.0, selCount  );

	{	do not close the progress}
	{	this will make VW use the progress for finish up work}
	{	so, 10% of the work will be VW finishing execution of the script,
		which normally is the time to reset parametric objects}

        ProgressDlgClose; {Due to a bug this is required prior Vectorworks 2017}

END;
RUN(TestProgressDlg);
```

## Python Script

### Example 1

Fake work by waiting and using a cancel-able dialog.

```python
hasCanceled = False

def TestProgressDlg():
	global hasCanceled
	
	def DoHalfTheWork():
		global hasCanceled
	
		kWORK = 26

		# we do 50% of the work in kWORK loops/calls to yield
		vs.ProgressDlgStart( 50.0, kWORK )
		
		i = 1;
		while (i <= kWORK) and (not hasCanceled):
			vs.Wait( 1 )	# well, we work by waiting
			
			vs.ProgressDlgYield( 1 )
			hasCanceled = vs.ProgressDlgHasCancel()

			i = i + 1
		
		vs.ProgressDlgEnd()


	vs.ProgressDlgOpen( "I'm about to do some heavy work", True )
	vs.ProgressDlgSetTopMsg( 'Top message to inform about something' )
	vs.ProgressDlgSetBotMsg( 'Bottom message to force the information in' )
	
	vs.ProgressDlgSetMeter( 'Doing the first half of the work...' )
	DoHalfTheWork()
	
	vs.ProgressDlgSetMeter( 'Doing the SECOND half...' )
	DoHalfTheWork()
	
	vs.ProgressDlgClose()

TestProgressDlg()
```

### Example 2

Resetting the selected objects with a progress dialog without cancel button.

```python
def TestProgressDlg():

	selCount = vs.NumSelectedObjects()

	def DoTheWork():

		# we do 90% of the work of resetting selected objects
		vs.ProgressDlgStart( 90.0, selCount )
		
		h = vs.FSActLayer()
		for i in range(selCount):
			vs.Wait( 1 )	#well, we work by waiting

			vs.ResetObject( h )

			h = vs.NextSObj( h )

			vs.ProgressDlgYield( 1 )
		
		vs.ProgressDlgEnd
	
	vs.ProgressDlgOpen( "I'm about to do some reset work", False )
	
	vs.ProgressDlgSetMeter( 'Resetting objects...' )
	DoTheWork()
		
	vs.ProgressDlgSetMeter( 'Finishing...' )
	vs.ProgressDlgStart( 10.0, selCount  )

	#	do not close the progress}
	#	this will make VW use the progress for finish up work
	#	so, 10% of the work will be VW finishing execution of the script,
	#	which normally is the time to reset parametric objects

	vs.ProgressDlgClose() # Due to a bug this is required prior Vectorworks 2017

TestProgressDlg()
