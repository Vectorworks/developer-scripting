The present article was originally published on the Techboard (2021.03.27): see the thread "python-plug-in-with-widgets-basic-example".  
I transfer it to the present wiki for fixing some mistakes and easier later maintenance.

by \_c\_  05:35, 1 January 2022 (EST)

# Plug-in with widgets, basic example (Python)

There was a question on the German VW forum about plug-ins with dividers and buttons. An ever recurring topic. I am (ever) switching to Python, and I thought that it could be a nice exercise for me to try it pythonically.

Please download the test files and expand them into your User's plug-in folder (there is no installer here):

[Test_PioWithWidgetsBasic.zip](examples/Test_PioWithWidgetsBasic.zip)

![pioWithWidget_img1.png](images/pioWithWidget_img1.png)

The Test PIO _c_ plug-in:

- uses an external file source (you don't need to script in the Plug-in Editor)
- is event enabled
- has a button triggering a script
- has dividers
- turns the dividers into expandable group widgets
- doesn't resolve text alignments, so that will take the active document's settings

I am new to Python and am sure that this can be done more efficiently, just take it as exercise.

## Imports

Once installed in the plug-ins folder, you can open it from: **Tools > Plug-ins > Plug-in Manager...** and choosing the `.vso` file. You will notice that the code uses imports (= includes in Vectorscript Pascal):

![pioWithWidget_img3.png](images/pioWithWidget_img3.png)

- **`import vs`**: relative path from the script options to the file `vs.py`. This enables the odd 3000 Vectorscript routines to the script editor you use for coding. More about using an IDE [here](../../../Python/README.md#ide-and-debugging-python-scripts).
- **`import example`**: relative path from the `.vso` file to the code file `example.py`, which contains the code for this plug-in.
- **`vs.SetPref(412, False)`**: disables the cache for this plug-in. If you work on Python using external files - vs. inside the plug-in editor - you will need to reload the code at every change, but Python has a cache preventing this. With the flag `412` you can turn off caching during development.
- **`example.execute()`**: "execute" is the name of the main routine available in the file "example". You could also call it "main" or whatever you wish.

## Events

The present plug-in wants to be event enabled: you enable events in the Options tab of the Plug-in editor:

![pioWithWidget_img2.png](images/pioWithWidget_img2.png)

### Event list

There are bucketloads of events, you'll find them in the SDK (`Source\SDKLib\Include\Kernel\MiniCadHookIntf.h`) and it does take a lot of time to be comfortable with their usage. Some of them I have really no idea what they do, and believe me, I did spend an inordinate amount of time on them. The two major files you might want to study are these below, but there is far more (the SDK version in the screenshots is irrelevant):

![pioWithWidget_img4a.png](images/pioWithWidget_img4a.png)

![pioWithWidget_img4b.png](images/pioWithWidget_img4b.png)

### Event parsing

The code runs a number of times (and double as much if the developer mode is on), once for every event. There are at least 3 events, but you can add many more:

- **`kObjOnInitXProperties` (5)**: extended properties, runs BEFORE `kParametricRecalculate`
- **`kParametricRecalculate` (3)**: the plug-in regenerates, here you'll put the actual code
- **`kObjOnWidgetPrep` (41)**: after clicking on an obj, for building its OIP, it runs AFTER `kParametricRecalculate`

### Custom Object Info (obj variables)

You must limit the execution of the code as far as possible and make sure that it runs on the proper object handles. The routine [`vs.GetCustomObjectInfo`](VS:GetCustomObjectInfo) fetches the needed variables.

```python
(ok, gPio_N, gPio_H, gPioRec_H, gWall_H) = vs.GetCustomObjectInfo()
# gPio_N = name of the plug-in
# gPio_H = handle to the running plug-in (what is selected in the OIP)
# gPioRec_H = handle to the plug-in record (default values, plug-in definition, as displayed in the plug-in's mode bar)
# gWall_H = handle to the wall gPio_H is inserted into, if any
```

### Event Info (obj events)

Every time the code runs, you must parse the type of event and run the right code during the right event. [`vs.vsoGetEventInfo`](VS:vsoGetEventInfo) fetches event info:

```python
(theEvent, theButton) = vs.vsoGetEventInfo()
# note: theButton is a generic message, not necessarily a button

(theEvent, aMessage) = vs.vsoGetEventInfo()
```

### Init properties

During the init properties event (5) you set up the Object Info Palette behaviour and other things:

```python
if theEvent == kObjOnInitXProperties: # event 5
    # init event behaviour for the plug-in, for example:
    ok = vs.SetObjPropVS(kObjXPropHasUIOverride, True) # constant 8
```

### Collapsable/Expandable Widgets

If you want to use widget groups, buttons or custom pull-down menus you need to turn on UI override using the constant `kObjXPropHasUIOverride` (8):

```python
ok = vs.SetObjPropVS(kObjXPropHasUIOverride, True) # constant 8
```

To have the lovely widget groups in expanded/collapsed state you must add the char `kWidgetGroupMode` (81) and set it to `automatic` (2):

![pioWithWidget_img5a.png](file:pioWithWidget_img5a.png) ![pioWithWidget_img5b.png](file:pioWithWidget_img5b.png)

- enable widget groups with [`vs.SetObjPropCharVS`](VS:SetObjPropCharVS):

```python
ok = vs.SetObjPropCharVS(kWidgetGroupMode, vs.Chr(kWidgetGroupAutomatic), True)
```

- add parameters to the plug-in as static text (the items named `__div...` in the screenshot)
- turn the static text into separators using [`vs.vsoInsertWidget`](VS:vsoInsertWidget) and passing the widget type `kWidgetSeparator` (100):

```python
ok = vs.vsoInsertWidget(cP___div0 -1, kWidgetSeparator, cP___div0, 'parameter name', empty)
```

![pioWithWidget_img6.png](file:pioWithWidget_img6.png)

The routine [`vs.vsoInsertWidget`](VS:vsoInsertWidget) requires a string where you'll pass a parameter name, ideally optimised for OIP display. Most times you will have thus different strings for universal and localised parameter names. The function [`vs.GetLocalizedPluginParameter`](VS:GetLocalizedPluginParameter) fetches the localised name passing the universal one. Since it returns two values, a boolean and a string, it cannot be used directly, so I created one simple sub named `O_GetLocParmName` which returns only the string:

```python
def O_GetLocParmName(pioRecName, univParmName):
    (boo, locParmName) = vs.GetLocalizedPluginParameter(pioRecName, univParmName)
    return locParmName
```

We add indenting levels in a loop using [`VS:vsoWidgetSetIndLvl`](VS:vsoWidgetSetIndLvl). Note: This turns the widgets into expandable widgets.
Important: Don't omit to set the 0-levels, or things are going to mess up:

```python
titles = [cP___div0, cP___div1, cP___div2]
for i in range(vs.NumFields(gPioRec_H) +1):
    if (i in titles): 
        vs.vsoWidgetSetIndLvl(i, 0)
    else:
        vs.vsoWidgetSetIndLvl(i, 1)
```

; Warning:  to see widget groups display properly, you will need either to close/open the document or the script editor EVERY time you change something in the parameter index list (add, delete parameters)

### Custom Pull-down menu Widgets

IF, and only IF,  you also want to use custom pull-down menus loading custom values, you will also need to enable custom widget visibilities.

: Note: If you do this, as of VW 2021 you cannot use [SetParameterVisibility](../../../Function%20Reference/Functions/SetParameterVisibility) or [EnableParameter](../../../Function%20Reference/Functions/EnableParameter), which needs parameter ''names''. You can only use [vsoWidgetSetVisible](../../../Function%20Reference/Functions/vsoWidgetSetVisible) and [vsoWidgetSetEnable](../../../Function%20Reference/Functions/vsoWidgetSetEnable) which need parameter ''indexes'', so you must keep track of the parameter indexes and store them somehow as file. This does add complexity (I have a sub auto-filling a list as text into the right place).

```python
vs.SetObjPropVS(kObjXHasCustWidgetVisibilities, True); 
# not used in the test example:
# only needed for custom pull-down menus with special lists of values
# after enabling this prop you need to set visibilities during event kObjOnWidgetPrep
```

## Note about Text Alignment

You can set a plug-in object to respond to font and text size using 
```python
vs.SetObjectVariableBoolean(gPio_H, 800, True) 
```

but all other text properties, such as horizontal and vertical alignment, etc. must be coded and driven by parameters.
