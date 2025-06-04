# GetName

## Description
Function GetName returns the object name of the referenced object. The function returns "None" if the object has no object name.

A handle to layer may not passed to this routine; to obtain a layer name, use [[VS:GetLName| GetLName]].

```pascal
FUNCTION GetName(h : HANDLE): STRING;
```

```python
def vs.GetName(h):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
[[User:CBM-c-|_c_]] (2016.02.18): If the string 'none' is returned (and not 'None' as stated above) this is not localized. Checked in the German VW.

(Unsigned): 
This function is a little non-intuitive. If the namestring of object h is empty, this function returns the literal string "none". I don't know what the localization implications of this are.

If the name has been deleted it returns an empty string, so test for both (empty string or "none" string).

## Examples
#### VectorScript ####
```pascal
ObjectName := GetName(HandleToObject);
```
#### Python ####
```python
ObjectName = vs.GetName(vs.FSActLayer())
```

## See Also
VS Functions:
[SetName](SetName.md)

## Version
Availability: from All Versions

## Category
* [Object Names](../Categories/Object%20Names.md)
