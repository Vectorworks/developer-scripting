# GetEnabledModules

## Description
Determines which combination of product modules are currently enabled.  

This function returns a LONGINT value which contains a bit for each possible product module.  If a module is enabled, then the corresponding bit will be set to 1.  If that module is disabled, then its bit will be 0.  The table below contains selectors that can be used to interpret the results of this function.  To determine if a module is enabled, do a bitwise &quot;and&quot; operation with the selector and the value returned by this function.  See the usage example below.

{| class="wikitable_c"
|+ Table - GetEnabledModules Selectors
! Module 
! Selector 
! Description 
|-
| Foundation
| style="text-align:center" | 0
| VectorWorks general purpose CAD.
|-
| RenderWorks
| style="text-align:center"| 1
| Advanced rendering features, lighting, textures.
|-
| Architect
| style="text-align:center"| 2
| Architectural features including advanced window, door, wall framing, HVAC
|-
| Landmark
| style="text-align:center"| 4
| Site modeling and landscape design module. 
|-
| Spotlight
| style="text-align:center"| 8
| Theater lighting, set, and scenic design features.
|-
| Mechanical
| style="text-align:center"| 16
| Mechanical engineering module for designers and fabricators. 
|-
| Pro
| style="text-align:center"| 32
| Foundation for European market. 
|}

```pascal
FUNCTION GetEnabledModules : LONGINT;
```

```python
def vs.GetEnabledModules():
    return LONGINT
```

## Examples
#### VectorScript ####
```pascal
PROCEDURE testModules;

{----------------------------------------------------------}
FUNCTION bittest(value, mask :LONGINT) :BOOLEAN; 
VAR 
bit :INTEGER; 
BEGIN 
bittest := FALSE; 
bit := 31;    { 2 ^ 31 is high order bit of a LONGINT argument. }
WHILE ((bit &gt; -1) &amp; (bittest = false)) DO BEGIN 
IF value &gt;= (2 ^ bit) THEN BEGIN 
value := value - (2 ^ bit); 
IF (2 ^ bit) = mask THEN bittest := TRUE; 
END; 
bit := bit - 1; 
END; 
END; 


{----------------------------------------------------------}
FUNCTION IsModuleEnabled(whichModule :LONGINT) :BOOLEAN; 
VAR 
enabledModules :LONGINT; 
BEGIN 
enabledModules := GetEnabledModules; 
IsModuleEnabled := bittest(enabledModules, whichModule)
END; 


BEGIN
IF IsModuleEnabled(4) &amp; IsModuleEnabled(1)  THEN BEGIN
{ Landmark and Renderworks are both enabled. } 
{ ... }
END;
END;
RUN(testModules);
```
#### Python ####
```python
def bittest (value, mask):
    bittest_result = False 
    
    bit = 31    #{ 2 ** 31 is high order bit of a LONGINT argument. }
    
    while ((bit > -1) and (bittest_result == False)):
        if value >= (2 ** bit):
            value = value - (2 ** bit) 
            if (2 ** bit) == mask:
                bittest_result = True 
        bit = bit - 1
         
    return bittest_result

#{----------------------------------------------------------}
def IsModuleEnabled(whichModule): 
	enabledModules = vs.GetEnabledModules()
	IsModuleEnabled = bittest(enabledModules, whichModule)
	return IsModuleEnabled

def testModules():
	if IsModuleEnabled(4) and IsModuleEnabled(1):
		pass
		#{ Landmark and Renderworks are both enabled. } 
		#{ ... }

testModules()
```

## See Also
VS Functions:
[DisableModules](DisableModules.md)

## Version
Availability: from VectorWorks 10.0

## Category
* [Utility](../Categories/Utility.md)
