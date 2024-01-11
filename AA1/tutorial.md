Update Keylogger to Handle Arrow Keys
======================
In this activity, you will code to modify the keylogger to detect arrow keys.


<img src= "https://s3-whjr-curriculum-uploads.whjr.online/f4bbaeac-7ead-4021-a72a-3c706d3af2e9.gif" width = "auto" height = "auto">


Follow the given steps to complete this activity.


1. Open `main.py` file.
2. In the `onPress()` function, print the `key` variable to check which key is pressed.
    ```
    print(key)
    ```
3. Check which arrow key is pressed and accordingly add text `(RIGHT_ARROW)`, `(LEFT_ARROW)`, `(UP_ARROW)`, `(DOWN_ARROW)`.
    ```
    elif key == keyboard.Key.right:
        text += " (RIGHT_ARROW) "
    elif key == keyboard.Key.left:
        text += " (LEFT_ARROW) "
    elif key == keyboard.Key.up:
        text += " (UP_ARROW) "
    elif key == keyboard.Key.down:
        text += " (DOWN_ARROW) "
    ```
   


Save and run the code to check the output.
