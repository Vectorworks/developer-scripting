# VerifyLibraryRoutine

## Description
Verifies that a procedure or function call located in a VectorScript extension is registered and available for use in scripts.

Call this function prior to using any call located in a VectorScript extension to ensure successful use of the call in a script.

(A VectorScript extension is also known as an SDK Plug-in Library.  It is a plug-in that is developed using the VectorWorks SDK and the C++ language.  When installed in the Plug-ins folder it provides functions that may be called from VectorScript.  The VerifyLibraryRoutine function allows the script to determine if the function is available.)

```pascal
FUNCTION VerifyLibraryRoutine(routineName : STRING): BOOLEAN;
```

```python
def vs.VerifyLibraryRoutine(routineName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|routineName|STRING|Name of function call to be verified.|

## Remarks
([[User:CBM-c-|_c_]], 2016.01.02):  
* The routines parsed are only those that you'll find in the VWPluginLibraryRoutines.p file. Any other will return FALSE!
* This is the only function that doesn't accept a variable of type string. It really only accepts a routine name within quotes:
<code lang='vs'>
 boo := VerifyLibraryRoutine('PythonExecute'); { OK }

 routineName := 'PythonExecute';
 boo := VerifyLibraryRoutine(routineName); { error }
```

([[User:CBM-c-|_c_]], 2015.06.14):  This can be used to test the routine in the .p files suppressing warnings. Suppose you script for VW 2013 but wish to use a routine developed for VW 2014, normally the parser would rise the error "identifier not declared" since the routine is unknown (introduced later). If you wrap the routine call into an IF condition starting with VerifyLibraryRoutine this warning is suppressed.

; Exception: the warning "The function is deprecated and should not be used" can't be suppressed! This will rise upon usage of routines listed as deprecated, for example the old dialog routines: [[VS:Vectorworks_2010_Deprecated_Functions| Deprecated for VW 2010 (10)]]

```pascal
{ try this in VW 15 (2010), where this routine would normally rise the error "identifier not declared" }
IF VerifyLibraryRoutine('XMLSAXAddNodeAttr') = FALSE THEN
    AlrtDialog(Concat('No, forget it, it won''t work in the user''s VW version'))
ELSE
    XMLSAXAddNodeAttr(XMLHandle, nodeVal); { XMLSAXAddNodeAttr was introduced by VW 16 (2011) }
```

; Python: this function does not work in Python scripts in Vectorworks 2017 and older. Instead, you can use Python functions to see if a function name is existing in the 'vs' module:
<code lang='py'>
hasattr( vs, 'FUNCTION_NAME' ) 
```

## Version
Availability: from VectorWorks 9.0

## Category
* [Utility](../Categories/Utility.md)
