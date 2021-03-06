# Noodle World
Many people enjoy eating noodles and pasta. There may be some recipes already shared on the Internet, but many people have their noodles and pasta recipes. The purpose of this project is to make it easy to upload their recipes and share them with others. 

## UX 

### Preview
- Desktop 

![MS_Capture_desktop](https://user-images.githubusercontent.com/53374745/88457662-8de9b800-ce88-11ea-9c50-5c635bcbfe5f.jpg)

- Tablet 

![MS_Capture_tablet](https://user-images.githubusercontent.com/53374745/89730044-7a6b4f00-da3b-11ea-94e9-bb81c3e9fd5d.jpg)

- Mobile 

![MS_Capture_mobile](https://user-images.githubusercontent.com/53374745/89730043-79d2b880-da3b-11ea-9c10-3172fad8163c.jpg)


### User scenario
1. An external user wants to see noodles recipes.
 - Ability to view the recipes: READ
2. An external user wants to add and share a recipe.
 - Use an add recipe form: CREATE
3. An external user wants to edit a recipe.
 - Every page has an “Edit Recipe” button and it has an edit form.: UPDATE
4. An external user wants to remove a recipe.
 - If the password is correct, anyone removes the recipe.: DELETE
5. An external user can send a message.
 - Use EmailJS 

### Wireframes
- [ms3-tablet.pdf](https://github.com/ss00831/milestone3/files/4977466/ms3-tablet.pdf)
- [ms3-desktop.pdf](https://github.com/ss00831/milestone3/files/4977467/ms3-desktop.pdf)
- [ms3-mobile.pdf](https://github.com/ss00831/milestone3/files/4977468/ms3-mobile.pdf)


## Features
 
### Existing Features 
- Preview: Maximum 4 recipes are shown on the main page(index.html).
- Recipes: List of the added recipes. I have used image cards.
- Add recipe: Create a new recipe.
- Edit recipe: Change and Update a recipe.
- Delete recipe
- Send Message: Use EmailJS API.


### Features Left to Implement
- Login function: At the moment, this project has not the login function; therefore I have made the recipe deletion password instead.


## Information Architecture

### Menu structure
![menu_structure](https://user-images.githubusercontent.com/53374745/88479081-129e0a00-cf4d-11ea-9eb4-12c8fe5a5187.png)

### Database
0. The database of this project is based on MongoDB.
1. Database name : NoodleCollection
2. Collections
 - recipes

| Field Name   | Input data type | Data type |
|--------------|-----------|-----------|
| _id          | ObjectId  | ObjectId  |
| recipe_name  | text    | String    |
| nationality  | text    | String    |
| portions     | number    | String    |
| difficulty   | select    | String    |
| ingredients  | text     | Array    |
| instructions | text     | Array    |
| photo_url    | text    | String    |
| del_password | password    | String    |

 - difficulty : User can not add/edit this collection.

| Field Name | Field Value | Data type |
|------------|-------------|-----------|
| difficulty | Difficult   | String    |
| difficulty | Normal      | String    |
| difficulty | Easy        | String    |


## Technologies Used

### Language
- HTML5
- CSS3 
- JavaScript
- Python

### Tools & Libraries 
- Flask 1.1.2 (https://flask.palletsprojects.com/en/1.1.x/)
- MongoDB 4.2.8 (https://www.mongodb.com/)
- JQuery 3.5.1 (https://jquery.com)
- Materializecss 1.0.0 (https://materializecss.com/)
- Fontawesome 5.12.1 (https://fontawesome.com/)
- Google font (https://fonts.google.com/)
- Github (https://github.com/)
- Gitpod (https://www.gitpod.io/)
- Heroku (https://www.heroku.com/): For deployment

### APIs
- Email JS (http://emailjs.com/)


## Testing (*)
0. Device / Browser spec
- For Usability testing

|              |            Device 1            |               Device 2               |     Device 3     |                 Device 4                 |         Device 5        |
|:------------:|:------------------------------:|:------------------------------------:|:----------------:|:----------------------------------------:|:-----------------------:|
| Device Model |         Macbook Air 13"        |           Samsung NT900X5W           |   iPhone XS Max  |                iPad Air 2                |    LG V30S (LG-H930)    |
|      OS      |     macOS Catalina 10.15.3     |      Windows 10 Home 10.0.19041      |    iOS 13.5.1    |                iOS 13.5.1                |        Android 9        |
|      CPU     | Intel core i5 1.6GHz Dual-Core | Intel core i5-7200 2.50GHz Dual core | Apple A12 Bionic | 1.5GHz tri-core 64-bit ARMv8-A "Typhoon" | Qualcomm Snapdragon 835 |
|      RAM     |               4GB              |                  8GB                 |        4GB       |                    2GB                   |           6GB           |
|    Graphic   |     Intel HD Graphics 6000     |         Intel HD Graphics 620        |    APPLE G11P    |              PowerVR GXA6850             |   Qualcomm Adreno 540   |
|    Browser   |   Safari 13.0.5 (15608.5.11)   |          Chrome 84.0.4147.89         |      Safari      |                  Safari                  |   Chrome 84.0.4147.89   |


1. Code validation
- html (https://validator.w3.org/, Validate by URI): No error
* Note about index.html/recipes.html/singlerecipe.html 
 : If a Photo url field is blank, an error on each page.
   The error is "Bad value for attribute src on element img: Must be non-empty."
 : If I select "check by text input", it's no problem.  
- CSS (https://jigsaw.w3.org/css-validator/, Validate by direct input): No error
- JS (https://jshint.com/) 
 * function.js: 19 warnings
 * sendMessage.js: No error and warning.
- Python (http://pep8online.com/): No error

2. Usability Test
- All functional test cases (68 items): All pass
- Input data test cases (47 items) + delete password test (15 cases): All pass
+) 07/30/2020: Due to take away the password field in editrecipe.html (edit_recipe), the test cases have reduced.
+) 08/04/2020: Added the 15 cases for deletion test

3. Responsive & Browser Test
- Pass condition :
    1. Must be resized to the image and content by the window sizes and resolutions
    1. All links need to work like the Full test 
    1. All images/contents/links must not be broken.

| Browser\Resolution | >= 992 px | >= 768 px (Tablet size) | >= 600 px | >= 414 px (iPhone Plus) |>= 320 px (iPhone 5/SE)|
|:-------:|:-------:|:-----------------:|:--:|:--: |:--: |
| Safari        | Pass       |  Pass    | Pass   | Pass | Pass |
| Chrome        | Pass       |  Pass    | Pass   | Pass | Pass |
| Firefox       | Pass       |  Pass    | Pass   | Pass | Pass |
| Internet Explorer   | Pass       |  Pass    | Pass   | Pass | Pass |
| Edge          | Pass       |  Pass    | Pass   | Pass | Pass |


- For responsive & browser testing

| Browser | Version | Device Model Name | OS |
|:-------:|:-------:|:-----------------:|:--:|
| Safari        | 13.1.2 (15609.3.5.1.3)        |  Macbook Air 13"                 | macOS Catalina 10.15.6   |
| Chrome        |  84.0.4147.89        |  Samsung NT900X5W                 | Windows 10 Home 10.0.19041   |
| Firefox        | 78.0.2 (64bits)        |  Samsung NT900X5W                 | Windows 10 Home 10.0.19041   |
| Internet Explorer        | 11.959.18362.0        | Samsung NT900X5W                  | Windows 10 Home 10.0.19041   |
| Edge        | 84.0.522.44        | Samsung NT900X5W                  | Windows 10 Home 10.0.19041   |

4. The detailed result : Please refer the test sheet as below.

[rev05_testcases_20200731.xlsx](https://github.com/ss00831/milestone3/files/5005866/rev05_testcases_20200731.xlsx)


5. Bugs
- index.html (/get_index): If a recipe has a long recipe title, the nationality is not visible.

![bugid2](https://user-images.githubusercontent.com/53374745/89405003-27cc2300-d71b-11ea-86a8-95a4b00d5575.png)

+) 08/09/2020: Recipe name field - Fixed to maximum 60 characters, added auto break line on indexh3 class and card-title class

- addrecipe.html (/add_recipe) and editrecipe (/edit_recipe) : (Only for Apple products) Only the Safari built-in button works correctly. Please refer to the pictures below.

Custom HTML select tag :

![bug3-1](https://user-images.githubusercontent.com/53374745/89729327-dc748600-da34-11ea-9b72-76113ecb23ed.jpg)

Safari built-in select button : 

![bug3-2](https://user-images.githubusercontent.com/53374745/89729328-dd0d1c80-da34-11ea-82c0-2d2e3f954e72.jpg)

### Testing history
1. 29 Jul 2020 - Created the test cases for functional, responsive & browser testing
2. 30 Jul 2020 - Functional, input data, responsive & browser testing
3. 31 Jul 2020 - Functional, input data testing
4. 4 Aug 2020 - Functional, input data and deletion testing
5. 6 Aug 2020 - Deletion testing : Check the changed error message
6. 8 Aug 2020 - Check indexh3 and card-title class
7. 10 Aug 2020 - Functional, input data, responsive & browser testing

## Deployment

### My Milestone3 page address : https://noodleworld-ms3.herokuapp.com/

### To deploy this page to GitHub Pages from its GitHub repository (https://github.com/ss00831/milestone3) :
1. Create "requirements.txt" file
```
pip3 freeze > requirements.txt
```
2. Create "Procfile" file
```
echo web: python3 app.py > Procfile
```
3. Login heroku
4. Setting Config Vars 
: Heroku homepage - Select "noodleworld-ms3" project - Setting - Click "Reveal Config Vars" - Create Config Vars as below and save
![heroku_setting](https://user-images.githubusercontent.com/53374745/88460288-62bc9400-ce9b-11ea-895b-32e483e55d29.JPG)

* You can find the ["MONGO_URI"] value as below
: Login MongoDB - Select your cluster - click "CONNECT" button - click "Connect your application" - Select your driver and version - Copy the url - Paste in the env.py file
+) The url example: "mongodb+srv://root:xxxx@myfirstcluster-xxxxx.mongodb.net/COLLECTIONNAME?retryWrites=true&w=majority".
5. Deploy to Heroku
- git add . 
- git commit -m "commit comment" 
- Check a linked remote: git remote -v 
- (If it doesn't exist any linked remote) To link a remote: git remote add heroku https://git.heroku.com/noodleworld-ms3.git
- git push -u heroku master
6. To scale dynos 
```
heroku ps:scale web=1 
```
7. Run the webpage: Click "Open app" button on the Heroku dashboard page or write https://noodleworld-ms3.herokuapp.com/ on your web browser.

### How to run this project locally

To clone this project from GitHub :
1. Click [Code] - [Download ZIP] on the repository page.
2. Unzip the milestone3-master.zip file.
3. Open Git Bash on your local IDE.
4. (Optional) Change the current working directory to the location where you want the cloned directory to be made.
5. Move to the milestone3-master folder
6. Install the requirement files as below.
```
pip3 install -r requirements.txt
```
* If you need, update pip.
```
python -m pip install --upgrade pip
```
7. Make "env.py" file and write as below in the file.
```
import os

os.environ["SECRET_KEY"] = "YOUR_SECRET_KEY"
os.environ["MONGO_DBNAME"] = "MONGO_DB_COLLECTION_NAME"
os.environ["MONGO_URI"] = "your_mongodb_url"
```

* You can find the ["MONGO_URI"] value as below
: Login MongoDB - Select your cluster - click "CONNECT" button - click "Connect your application" - Select your driver and version - Copy the url - Paste in the env.py file
+) The url example : "mongodb+srv://root:xxxx@myfirstcluster-xxxxx.mongodb.net/COLLECTIONNAME?retryWrites=true&w=majority".

8. Execute the command as below for running app.py. 
```
flask run
```
9. Open a web browser and write this address as below.
```
http://127.0.0.1:5000/
```
## Credits

### Content
1. Short information about noodle : https://en.wikipedia.org/wiki/Noodle

### Media
1. Main image : https://pixabay.com/sv/photos/nudlar-om-mat-ramen-gravy-1962270/

2. Short information background : https://pixabay.com/sv/photos/pasta-nudlar-livsmedel-k%C3%B6k-549108/

3. E-mail icon background: https://www.netclipart.com/down/wThTii_e-mail-png-free-download-transparent-background-emails/

4. Alternative image for recipe : https://icon-icons.com/download/124121/PNG/512/

### Acknowledgements

1. How to create inline list in materialize css 
 - https://stackoverflow.com/questions/42884750/how-to-create-inline-lists-in-materializecss
2. Add/Remove Input Fields Dynamically with jQuery 
 - https://www.sanwebe.com/2013/03/addremove-input-fields-dynamically-with-jquery
3. How TO - Position Text Over an Image 
 - https://www.w3schools.com/howto/tryit.asp?filename=tryhow_css_image_text
4. Use an alt image for img HTML tags 
 - https://coderwall.com/p/hxauyq/use-an-alt-image-for-img-html-tags
5. Check if a given key already exists in a dictionary
 - https://stackoverflow.com/questions/1602934/check-if-a-given-key-already-exists-in-a-dictionary
6. How to append existing array in existing collection in mongodb using java with new values
 - https://stackoverflow.com/questions/31956696/how-to-append-existing-array-in-existing-collection-in-mongodb-using-java-with-n
7. loop backwards using template 
 - https://stackoverflow.com/questions/12680691/loop-backwards-using-django-template
8. materialize grid s12 not working in mobile view 
 - https://stackoverflow.com/questions/42891630/materialize-grid-s12-not-working-in-mobile-view/42912833
9. How to validate select option for a Materialize dropdown?
 - https://stackoverflow.com/questions/34248898/how-to-validate-select-option-for-a-materialize-dropdown
10. Table generator 
 - https://www.tablesgenerator.com/markdown_tables
11. Auto break line in HTML
 - https://stackoverflow.com/questions/5852700/auto-break-line-in-html