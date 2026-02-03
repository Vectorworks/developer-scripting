# PythonExecute

## Description
Execute the given python script.

You can use 'include' in python to run additional code in python files. However, before you execute the script make sure the python file are foundable through the PythonGetSearchPath. Use PythonSetSearchPath to change it.

; Note: Scripts executed via this function should not contain User Interactive functions like GetPt for example.

```pascal
PROCEDURE PythonExecute(script : DYNARRAY[] of CHAR);
```

```python
def vs.PythonExecute(script):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|script|DYNARRAY[] of CHAR|The script to be executed.|

## Examples
An example of a simple VectorScript that runs a python script:
```pascal
PROCEDURE Example;
VAR
  strName : STRING;
BEGIN
  strName := 'vs string';
  
  PythonBeginContext;
  PythonExecute( 'import vs' );
  PythonExecute( 'ss = ''hello from python: ''' );
  PythonExecute( 'vs.AlrtDialog(ss + vs.GetVSVar("strName"))' );
  PythonExecute( 'vs.SetVSVar("strName", "python string")' );
  PythonEndContext;
  
  AlrtDialog( Concat( 'VectorScript received: ', strName ) );
END;
RUN(Example);
```
You can use PythonExecute to send a Python script to VW via AppleScript:
```applescript
tell application "BBEdit"
        set thePyScript to contents of front window
        set thePyScriptLines to paragraphs of thePyScript
        set theScript to "
            Procedure RunPython;
            VAR
                pyScript :DYNARRAY [] OF CHAR;
       
            BEGIN
            pyScript := '';
            PythonBeginContext;
    "
        repeat with i from 1 to number of items in thePyScriptLines
            set scriptLine to item i of thePyScriptLines
            set theScript to theScript & "pyScript := Concat(pyScript, '" & scriptLine & "', '" & return & "');" & return
        end repeat
    
        set theScript to theScript & "
            PythonExecute(pyScript);
            PythonEndContext;
            END;
            Run(RunPython);
            "
    end tell
    
    tell application "Vectorworks 2014"
        activate
        DoScript theScript
    end tell
```

## See Also
VS Functions:
[PythonGetSearchPath](PythonGetSearchPath.md) 
| [PythonSetSearchPath](PythonSetSearchPath.md) 
| [PythonBeginContext](PythonBeginContext.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
