# GetVersionEx

## Description
Returns version information about the Vectorworks application. Parameter major returns the major version number of the application. Parameters minor and maintenance return minor version information. Parameter platform returns the OS platform on which Vectorworks is running (1 = Macintosh, 2 = Windows).<BR>
Parameter buildNum returns the build number of the version.<BR>
<BR>
Vectorworks 2008 has version major number 13, 2009 - 14 and so on.<BR>
<BR>
For example:<BR>
<BR>
Vectorworks 2010.0.1 running on a Macintosh would return:<BR>
<BR>
major: 15<BR>
minor: 0<BR>
maintenance: 1<BR>
platform: 1<BR>
buildNum: 95668<BR>

```pascal
PROCEDURE GetVersionEx(
				VAR major       : INTEGER;
				VAR minor       : INTEGER;
				VAR maintenance : INTEGER;
				VAR platform    : INTEGER;
				VAR buildNum    : LONGINT);
```

```python
def vs.GetVersionEx():
    return (major, minor, maintenance, platform, buildNum)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|major|INTEGER|Returns major version number of application.|
|minor|INTEGER|Returns minor version number of application.|
|maintenance|INTEGER|Returns maintenance version number of application.|
|platform|INTEGER|Returns platform of application.|
|buildNum|LONGINT|Returns the build number of application.|

## Examples
```pascal
PROCEDURE Example;
VAR 
	osMajor, osMinor, osIncr :LONGINT; 
	appMajor, appMinor, appMaint, platform :INTEGER;
	buildNum  :LONGINT;
	platformStr :STRING;
BEGIN
	GetVersionEx(appMajor, appMinor, appMaint, platform, buildNum);
	GetOSVersion(osMajor, osMinor, osIncr);
	IF (platform = 1) 
		THEN platformStr := 'MacOS'
		ELSE platformStr := 'Windows';
	Message('Vectorworks ', appMajor, '.', appMinor, '.', appMaint, ' build ', buildNum, ' running on ', platformStr, ' ', osMajor, '.', osMinor, '.', osIncr);
END;
RUN(Example);
```

## See Also
[GetVersion](GetVersion.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Utility](../Categories/Utility.md)
