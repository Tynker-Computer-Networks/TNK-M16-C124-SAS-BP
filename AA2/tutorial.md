Highlight the Email addresses in the Keylogger Text
======================
In this activity, you will code to highlight the email addresses if logged by the keylogger.


<img src= "https://s3-whjr-curriculum-uploads.whjr.online/ab822bab-1637-47f7-adfb-fb1184346b74.gif" width = "auto" height = "auto">


Follow the given steps to complete this activity.


1. Open `main.py` file.
2. Define `highlight_emails()` function, that will take the text logged by keylogger and modify it to highlight the emails and return the modified text.
   * Define `highlight_emails()` function that takes one parameter `text`
    ```
    def highlight_emails(text):
    ```
   * Split the text into an array of words.
    ```
    words = text.split(" ")
    ```
    * Create an empty list `modified_words` where we will store the updated words.
    ```
    modified_words = []
    ```
    * Go through every word.
      *  Check if `@`, `.com` exits in the word and `*` does not to check if the word is an email.
      *  if yes then add `*` to both sides of the word to make it bold.
      *  Append the word in modified list
    ```
    for word in words:
        if '@' in word and '.com' in word and '*' not in word:
            modified_words.append('*' + word + '*')
        else:
            modified_words.append(word)
    ```
    * Join `modified_words` list to create a string `modified_text` and return it.
    ```
    modified_text = ' '.join(modified_words)
    return modified_text
    ```
3. Call `highlight_emails()` function and update the `text` in the `on_press()` function.
    ```
    text = highlight_emails(text)
    ```
   


Save and run the code to check the output.
