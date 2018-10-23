# Build a live comment with sentiment analysis using Flask, Vue and Channels

This is a demo application showing how to build a live comment with sentiment analysis using Flask, Channels and Vue. You can read the tutorial on how it was built [here](https://pusher.com/tutorials/flask-vue-comments)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

This application uses the following:

 - Python 3.6 (You should have python 3.6 or higher version installed)
 - Pusher Channels (Create an account [here](https://dashboard.pusher.com/accounts/sign_up) or [login](https://dashboard.pusher.com/accounts/sign_in) here)
 - Vue

### Setting up the project

First, clone this repository to your local machine:

```sh
 $ git clone https://github.com/dongido001/live-comment-sentiment.git
```

 Next update the following keys in the `.env` file with your correct Pusher keys:
  ```
  PUSHER_APP_ID=app_id
  PUSHER_KEY=key
  PUSHER_SECRET=secret
  PUSHER_CLUSTER=cluster
  ```

  Finally, update the placeholder - `<PUSHER_KEY>` and `<PUSHER_CLUSTER>` with your correct Pusher Key in `/static/custom.js` file.

    ```javascript
        // Initiatilze Pusher JavaScript library
        var pusher = new Pusher('<PUSHER-APP-KEY>', {
            cluster: '<CLUSTER>',
            forceTLS: true
        });
    ```

### Running the App

To get the app running:

 - From a command line, make sure you are in the project's root folder
 - Create a virtual environment:
 ```
 python3 -m venv env
 ```
 - Activate the virtual environment:
 ```
   source env/bin/activate
 ```
 On windows? Activate it with the below:
 ```
   env/Scripts/activate
 ```

 - Install the dependencies:
 ```
 pip install -r requirements.txt
 ```

 - Finally run the app:
 ```
  flask run
 ```

 Congrats! The app should now be running on http://localhost:5000.


- Open your browser and fire up the app - http://localhost:5000/ in two or more tabs.
- Add comments!

## Built With

* [Flask](http://flask.pocoo.org/) - A microframework for Python
* [Pusher](https://pusher.com/) - APIs to enable devs building realtime features
* [Vue](https://vuejs.org/) - Front-end framework for building user interfaces
