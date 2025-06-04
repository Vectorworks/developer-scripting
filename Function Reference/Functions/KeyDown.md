# KeyDown

## Description
Function KeyDown returns TRUE if a non-modifier keyboard character has been depressed. When TRUE is returned, the ASCII code of the character is returned.

Modifier keys are the Caps Lock, Command, Control, Option, and Shift keys.

```pascal
FUNCTION KeyDown(VAR asciiCode : LONGINT): BOOLEAN;
```

```python
def vs.KeyDown():
    return (BOOLEAN, asciiCode)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|asciiCode|LONGINT|ASCII code of key pressed.|

## Remarks
Using KeyDown (cCode) in a REPEAT...UNTIL loop such as the one that follows
will cause VectorWorks to hang. (Windows only).

<code lang="pas">
REPEAT
i := i + 1;
message ('i = ',i);
wait (1);
UNTIL KeyDown (keyCode);
</code>

If you have any scripts that use this, you had better check them.

<code lang="pas">
*******************************
*         Tom Urie            *
* Integrated Products Group   *
*        Vectorworks          *
*  vstanev@vectorworks.net    *
*******************************
</code>


I think that this is fixed in 901.



Also from Tom...
A word of warning:

The VectorScript function KeyDown () is initialized as TRUE on Windows in
9.5. Better check any scripts that use it.

Tom

## Examples
==== VectorScript ====
```pascal
WHILE NOT KeyDown(keyHit) DO
BEGIN
SysBeep;
SysBeep;
END;
Message('The key pressed was ',keyHit);
{an annoying example of one use of the KeyDown function}
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [User Interactive](../Categories/User%20Interactive.md)
