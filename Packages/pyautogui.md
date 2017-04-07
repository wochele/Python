# pyautogui

Automate mouse/keyboard

import pyautogui

# useful for entering text, newline is Enter
pyautogui.typewrite('Hello world!\n', interval=secs_between_keys)

# A list of key names can be passed too
pyautogui.typewrite(['a', 'b', 'c', 'left', 'backspace', 'enter', 'f1'], interval=secs_between_keys)

The full list of key names is in pyautogui.KEYBOARD_KEYS.

# Keyboard hotkeys like Ctrl-S or Ctrl-Shift-1 can be done by passing a list of key names to hotkey():
pyautogui.hotkey('ctrl', 'c')  # ctrl-c to copy
pyautogui.hotkey('ctrl', 'v')  # ctrl-v to paste

# Individual button down and up events can be called separately
pyautogui.keyDown(key_name)
pyautogui.keyUp(key_name)

https://pyautogui.readthedocs.io/en/latest/cheatsheet.html
