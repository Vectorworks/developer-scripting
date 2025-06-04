# AutoKey

## Description
Function AutoKey returns TRUE if a non-modifier keyboard character has been continually depressed for longer than the system defined key repeat rate. If a keyboard character has been continually depressed, then ASCII code of the character is returned in parameter asciiCode.

Modifier keys are defined as the Caps Lock, Command, Control, Option, and Shift keys.

```pascal
FUNCTION AutoKey(VAR asciiCode : LONGINT): BOOLEAN;
```

```python
def vs.AutoKey():
    return (BOOLEAN, asciiCode)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|asciiCode|LONGINT|The ASCII code of the key depressed.|

## Remarks
This function hangs on the Mac. Julian recommends using KeyDown on the Mac instead, while AutoKey works fine on the PC.



Today, under VW 13, it looks like the opposite is true:
*AutoKey will work (not reliably) under Mac, will hang on Windows
*KeyDown will sort of work under Windows, will be fully ignored under Mac

Note: tested on MacOs X.4.11 and Windows XP Pro, launching both routines from a dialog.
According to my tests, AutoKey under Windows will set the system to wait for user interaction, but at the same time makes the system blind to the user's interaction.

## Examples
#### VectorScript ####
```pascal
WHILE NOT AutoKey(keyHit) DO
BEGIN
SysBeep;
SysBeep;
END;
Message('The key pressed was ',keyHit);
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [User Interactive](../Categories/User%20Interactive.md)
