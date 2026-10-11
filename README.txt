HotkeyManager for Windows 11 (64-bit)

Start
-----
Double-click HotkeyManager.exe. No Visual Studio or project folder is needed.

User data
---------
By default, settings, hotkeys, custom commands, notes, and logs are stored in:
%LOCALAPPDATA%\HotkeyManager

Use Settings > Data storage to select another data directory. Existing user
data is not replaced by a new application build.

Dependencies and limitations
-----------------------------
The EXE includes the application, its GUI toolkit, and required keyboard
backend. No separate Python installation or internet connection is needed for
the regular GUI, hotkeys, built-in commands, or custom non-Python commands.

There is no embedded Python code editor. Python custom commands launch external
.py files and require a separately installed Python interpreter. Select
python.exe in the command settings, or ensure python.exe or the Windows py
launcher is available in PATH. PyInstaller does not provide a general-purpose
Python runtime for arbitrary user scripts.

Ollama is optional and must be installed separately. To run local-model
commands, install the selected model in Ollama first; the explicit built-in
model-download action requires an internet connection. Hotkeys and other
commands work without Ollama. The application does not bundle Ollama or its
models.

Errors
------
Startup exceptions are recorded in:
%LOCALAPPDATA%\HotkeyManager\logs\startup.log

If the app uses a custom storage directory or portable mode, the error dialog
shows the actual startup-log path. Runtime command errors are shown in the
application; a startup log is created only when application startup fails.
