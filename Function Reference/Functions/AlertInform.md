# AlertInform

## Description
Displays an alert dialog which provides the user an information about the result of a command.  It offers no user choices.

```pascal
PROCEDURE AlertInform(
				text       : STRING;
				advice     : STRING;
				minorAlert : BOOLEAN);
```

```python
def vs.AlertInform(text, advice, minorAlert):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|text|STRING|The information to be displayed.|
|advice|STRING|The text to be added in a smaller font under the main information message.|
|minorAlert|BOOLEAN|The severity of the alert: minor(true) or major(false).|

## Remarks
Created by 1/18/2005

## Examples
[AlertDialogsAndMessages](examples/AlertDialogsAndMessages.md)

```pascal
IF NOT sizeFound THEN
	AlertInform( Concat( GetPluginString( 3001 ), nominalSize ), '', TRUE );

	ELSE BEGIN
		SetRField (objHand, objName, paramName, Num2StrF (paramValue));
		alertMsg := Concat (locParamName, str1, Num2StrF (lowerLimit), str2, Num2StrF (upperLimit));
	END;
	AlertInform (alertMsg, '', TRUE);
END;	{of isError}

		{ Symbol definition: 16; SymListNode: 54 (Styled) }
		16, 54: if HANDLE_ClassesNMtrls( temp_h ) THEN;
		OTHERWISE
			AlertInform( GetPluginString( 3012 ), '', TRUE);
	END;	{of case container_type}
END;
```
```python
import vs

# Displays an alert dialog which provides the user an information about the
# result of a command.
text = 'Example text'
advice = 'Example'
minorAlert = True

vs.AlertInform(text, advice, minorAlert)
```

## See Also
VS Functions:
[AlertQuestion](AlertQuestion.md) 
| [AlertCritical](AlertCritical.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
