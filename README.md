## Custom Keybindings for VS Code

This document provides an overview of custom keybindings configured in Visual Studio Code (VS Code) to emulate the keybindings of Sublime Text 3. These keybindings enhance productivity by aligning VS Code's shortcuts with those familiar to Sublime Text 3 users.

### Go to Settings ###
Open the Command Palette:

On Windows and Linux, press Ctrl + Shift + P.
On macOS, press Cmd + Shift + P.
Search for "Preferences: Open Keyboard Shortcuts" and select it.

### Keybindings Overview

Below is a list of custom keybindings:

1. **Join Lines**  
   - **Key:** `Ctrl+J`  
   - **Command:** `editor.action.joinLines`  
   - **Context:** When focused on the text editor.

2. **Toggle Panel**  
   - **Key:** `Ctrl+Shift+J`  
   - **Command:** `workbench.action.togglePanel`  
   - **Context:** Global.

3. **Block Comment**  
   - **Key:** `Ctrl+Shift+/`  
   - **Command:** `editor.action.blockComment`  
   - **Context:** When focused on the text editor and it is not in readonly mode.

4. **Unbind Block Comment** (Removed Binding)  
   - **Key:** `Shift+Alt+A`  
   - **Command:** `-editor.action.blockComment`  
   - **Context:** When focused on the text editor and it is not in readonly mode.

5. **Copy Line Down**  
   - **Key:** `Ctrl+Shift+D`  
   - **Command:** `editor.action.copyLinesDownAction`  
   - **Context:** When focused on the text editor and it is not in readonly mode.

6. **Open Debug View**  
   - **Key:** `Shift+Alt+Down`  
   - **Command:** `workbench.view.debug`  
   - **Context:** When the debug view is enabled.

### JSON Keybindings

Copy and paste the following JSON code into your VS Code keybindings file:

```json
[
    {
        "key": "ctrl+j",
        "command": "editor.action.joinLines",
        "when": "editorTextFocus"
    },
    {
        "key": "ctrl+shift+j",
        "command": "workbench.action.togglePanel"
    },
    {
        "key": "ctrl+shift+/",
        "command": "editor.action.blockComment",
        "when": "editorTextFocus && !editorReadonly"
    },
    {
        "key": "shift+alt+a",
        "command": "-editor.action.blockComment",
        "when": "editorTextFocus && !editorReadonly"
    },
    {
        "key": "ctrl+shift+d",
        "command": "editor.action.copyLinesDownAction",
        "when": "editorTextFocus && !editorReadonly"
    },
    {
        "key": "shift+alt+down",
        "command": "workbench.view.debug",
        "when": "viewContainer.workbench.view.debug.enabled"
    },
]
