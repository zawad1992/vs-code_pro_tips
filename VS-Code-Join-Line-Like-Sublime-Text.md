# Creating a Shortcut Key in VS Code Similar to Sublime Text's Ctrl + Shift + J

In Visual Studio Code (VS Code), the shortcut key Ctrl + Shift + J, which is used in Sublime Text to join lines, does not exist by default.

However, you can create a custom keybinding to join lines, similar to Sublime Text's Ctrl + Shift + J. Follow these steps:

1. **Open the Command Palette**:
   - On Windows and Linux, press `Ctrl + Shift + P`.
   - On macOS, press `Cmd + Shift + P`.

2. **Search for "Preferences: Open Keyboard Shortcuts"** and select it.

3. **Create a New Keybinding**:
   - Click on the `{}` icon at the top right corner of the Keyboard Shortcuts page to open the `keybindings.json` file.
   - Add the following code snippet to create the new keybinding:

     ```json
     {
       "key": "ctrl+shift+j",
       "command": "editor.action.joinLines",
       "when": "editorTextFocus"
     }
     ```

   This sets Ctrl + Shift + J (or Cmd + Shift + J on macOS) as the shortcut for joining lines.

4. **Save and Close**:
   - Save the `keybindings.json` file and close it.

Now, you should be able to use Ctrl + Shift + J (or Cmd + Shift + J on macOS) in VS Code to join lines.
