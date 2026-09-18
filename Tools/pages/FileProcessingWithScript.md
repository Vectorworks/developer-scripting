# Purpose

Use to apply one script to multiple files. It will run Vectorworks, make it open each .vwx, .mcd and .sta files in a folder, and execute a script in each file.

# Disclaimer

This script is provided for advanced users and could have unintended consequences; use at your own risk.

# Instruction

## Windows

Download (Win): [File Open Test Tool (win only).zip](files/File%20Open%20Test%20Tool%20(win%20only).zip?download=true)

The tool comes with a python version and requires "psutil" and "tkinter" modules.

Copy the “File Open Test Tool” to your computer. Unzip and Click the <i>Run.bat</i>. 

## Mac

Download (Mac): [File Open Test Tool (mac only).zip](files/File%20Open%20Test%20Tool%20(mac%20only).zip?download=true)

You must have Python3 installed on your computer. The script will install the necessary modules.

Copy the “File Open Test Tool” to your computer. Unzip and run the <i>FileOpenToolMac.py</i> in a terminal:

```
cd <your folder>
python3 FileOpenToolMac.py
```

## How to use

Copy the 

This will open dos prompt to process vwx files executing a script.

![File Open Test Tool](files/File%20Open%20Test%20Tool.png)

This lauch Vectorworks and it will open each .vwx, .mcd and .sta files in the <i>Traverse</i> folder and execute the specified <i>script</i> (.vs - VectorScript; .py - Python). It will use the provided <i>Vectorworks</i> executable.

An 'Output'folder will be created next to the executable that contains the processed files (space holders, or saved VWX files after the script execution). The 'Output' folder will be used to skip already processed files in the Traverse folder.

A 'Crashed Files'folder will be created next to the executable that contains the crashed or timed out files.

The log file will be shown as text at the end of the tool execution.

The input is:
* Traverse Recursively Folder -- full path to the folder containing the source files for Vectorworks to open;
* Execute Script -- full path to the script that will be executed inside Vectorworks for each file (.vs - VectorScript; .py - Python)
* Vectorworks -- full path of the Vectorworks version that will be launched;
* Save VWX Files After Script Execution -- will save each open file in the 'Output' folder next to the Vectorworks app. When off, the 'Output' will contain place holder files so the <i>Continue From The Last Run</i> can work.
* Clear The Log File -- clear the log before running, or append to produce continuous log when multiple runs are necessary on the same input set.
* Continue From The Last Run -- turn on if there is alreayd an 'Output' folder. The tool will only process input files that are not present in the output. This is helpful if there is a crash and the processing stop, so you can continue with therest of the files.


# Pitfalls

The script runs Vectorworks with the <i>-ab</i> flag. Which removes all UI from being shown. This means that the script cannot show dialogs to collect information. The script must be self contained and be able to run without any input, or it should automat it's input externally.




