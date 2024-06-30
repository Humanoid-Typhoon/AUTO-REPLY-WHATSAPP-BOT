import pyautogui
import pyperclip
import time

# Coordinates for the starting and ending points of the selection
start_x, start_y = 663,216 
end_x, end_y = 1793,883

# Time delay to switch to the window where the selection needs to be made
time.sleep(3)

# Move the mouse to the starting position
pyautogui.moveTo(start_x, start_y)

# Click and hold the mouse button
pyautogui.mouseDown()

# Drag the mouse to the ending position
pyautogui.moveTo(end_x, end_y, duration=1)  # Duration can be adjusted as needed

# Release the mouse button
pyautogui.mouseUp()

# Press Ctrl+C to copy the selected text to the clipboard
pyautogui.hotkey('ctrl', 'c')
pyautogui.click(1793,883)

# Small delay to ensure the copy operation completes
time.sleep(0.5)

# Retrieve the copied text from the clipboard
copied_text = pyperclip.paste()

print("Copied text:", copied_text)
