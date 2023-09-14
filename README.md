<p align="center">   <img width="600" height="190" src="account/static/img/piclogo.png" alt="PicBookmark logo"/> </p>

## Description

PicBookmark is a Django-based social website for saving and sharing images from other websites. It allows users to create an account, save images they like from various websites, follow other users, and view images saved by others. It also features an activity stream and image views count functionality using Redis.

## Features
- **User Registration and User Profiles**: Users can create an account and set up their profiles, providing information about themselves and uploading a profile picture.

- **Social Authentication**: Users have the option to authenticate using their existing social media accounts, such as Google, making the registration and login process more convenient.

- **Image Bookmarking and Posting Images from Other Websites**: Users can bookmark and save images from the web by entering the image URL or using a browser bookmarklet.

- **User Likes, Follows, and Feed**: Users can like and bookmark images posted by other users. They can also follow other users to see their latest image posts in their personalized feed.

- **Activity Stream**: Users can view an activity stream that displays recent actions and updates from the users they follow, including new image uploads and likes.

- **Counting Image Views with Redis**: The platform utilizes Redis to track and count the number of views for each image. This feature allows users and image authors to see the popularity and engagement of their images.

## Development Mode
To set up the development environment, you need to follow these steps:

1. Ensure you have Python 3.x and Django installed. You can verify the installation by running the following commands:
   ```$ python --version```
   ```$ python -m django --version```
    If Django and Python are properly installed, you should see the version of your installation. If not, you'll get an error saying "No module named Django". If that's the case, you need to install Django using pip:

   ```$ pip install django```

2. Install postgres and create a database for the project. Save the credentials.

3. Install redis and run the server. Copy the host and port from the prompt.

4. Create a copy of the .env.example or renamed it to .env. Edit the file with your settings. 

5. You must keep the URL updated in the following files according to your domain:
    -   images/static/js/bookmarklet.js
    -   images/templates/bookmarklet_launcher.js

5. Clone the PicBookmark repository from GitHub and navigate into the project directory:
   ```$ git clone git@github.com/david96182/PicBookmark.git```
   ```$ cd PicBookmark```
6. Install the project dependencies:
   ```$ pip install -r requirements.txt```

7. Apply the migrations:
   ```$ python manage.py migrate```
8. Run the development server:
   ```$ python manage.py runserver```

After executing these steps, you can visit the application at http://127.0.0.1:8000/account with your web browser.

## How to Use

Once the development server is running, you can use the application by navigating to http://127.0.0.1:8000/account in your web browser. From there, you can register a new user account, log in, bookmark images, and interact with other users.

## Contributing

Contributions to PicBookmark are welcome! If you're interested in improving PicBookmark, you can follow these steps:

1. Fork the repository on GitHub.
2. Clone your forked repository to your local machine.
3. Make your changes and commit them to your forked repository.
4. Submit a pull request with your changes to the original repository.
5. Please ensure your code adheres to the existing style to keep the codebase as consistent as possible.
