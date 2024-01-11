Send and Listen the Keystroke Data
======================
In this activity, you will code to retrieve and display the data from the database whenever a new entry is made in the database.


<img src= "https://s3-whjr-curriculum-uploads.whjr.online/8ba1dde5-4f3b-408f-a15f-70ba79eccc58.gif" width = "auto" height = "auto">


Follow the given steps to complete this activity.


1. Create a `callback()` function that retrieve data when database is updated.
   * Open `app.py` file.
    ```
    def callback(event):
    global text
    if event.data:
        ref = db.reference('/keyboardData').get()
        text = ref
    ```
2. Create a reference to the database and a listener on this reference and call the `callback()` function.
    * Open `proxy-server.py`
    ```
    ref = db.reference('/keyboardData')
    ref.listen(callback)
    ```
   
3. Create route `/getData` which is called by our home page to get the data.
    * Open `proxy-server.py`
    ```
    @app.route('/getData', methods=["GET"])
    def getData():
        global text
        return jsonify(text)
    ```
   


Save and run the code to check the output.
