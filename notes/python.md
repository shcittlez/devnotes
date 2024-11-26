# Python Spacebar Counter Project

## Core Concepts

Python is a versatile, high-level programming language known for its readability and extensive library support. It is commonly used for web development, data analysis, machine learning, and building desktop applications.

### Key Concepts from Project

1. **Tkinter for GUI**
   - Tkinter is Python's built-in library for creating graphical user interfaces (GUIs).
   - It allows you to create windows, buttons, labels, and other UI elements.

2. **Keyboard Library**
   - The `keyboard` library enables global hotkey detection, allowing programs to respond to keypresses even when the application is not in focus.

3. **Event-Driven Programming**
   - Python supports event-driven programming, where functions are triggered by user actions (like pressing keys or clicking buttons).

4. **Executable File Creation**
   - You can use `PyInstaller` to bundle Python scripts into standalone executable files (`.exe`), allowing others to use the program without installing Python.

## Code Examples

### 1. Counting Spacebar Presses

This example tracks the number of times the spacebar is pressed using the `keyboard` library and updates the count in a GUI window:

```python
import keyboard
from tkinter import Tk, Label

class CounterApp:
    def __init__(self, root):
        self.count = 0
        self.root = root
        self.root.title("Spacebar Counter")
        self.label = Label(root, text=f"Count: {self.count}", font=("Helvetica", 24))
        self.label.pack(pady=20)

        # Spacebar increments count
        keyboard.on_press_key("space", self.increment_count)

    def increment_count(self, event):
        self.count += 1
        self.label.config(text=f"Count: {self.count}")

if __name__ == "__main__":
    root = Tk()
    app = CounterApp(root)
    root.mainloop()
```

### 2. Saving and Viewing Counts

This example demonstrates how to save spacebar counts and display them in a history window:

```python
def reset_count(self):
    self.history.append(self.count)
    self.count = 0
    self.update_label()
```

### 3. Packaging an Application

You can create a standalone executable file from your Python script using PyInstaller:

```bash
pyinstaller --onefile --windowed --icon="your_icon.ico" global_spacebar_counter.py
```

## Resources

- [Tkinter Documentation](https://docs.python.org/3/library/tkinter.html)
- [Keyboard Library](https://github.com/boppreh/keyboard)
- [PyInstaller Guide](https://pyinstaller.org/en/stable/)
- [Python Official Website](https://www.python.org/)
