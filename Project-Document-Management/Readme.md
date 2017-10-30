# Project 

In this project we are going to be working with zip files, images and the files system.
We are given a contract to develop an MVP for a image viewing app. The app should display a list of collages of images and when tapped, display all the images for a particular collection.

**Parameters**
1. We should first hit the API do get the collections (https://api.myjson.com/bins/1165qr)
2. The json response has an array of collection with a url to a zip file for each collection.
3. We want to download the zip files and unzip them to a temporary store.
4. We want to display the preview images (_preview.png) and the name of the collection in a list
5. When a user taps a collection, we want to display the images for that collection.


## Milestones

- [x] Download the collections from this url. https://api.myjson.com/bins/1165qr
- [x] Parse the json into models
- [x] Download the zip files from the models
- [x] Unzip the zip files containing the images into a temporary store
- [x] Display the thumbnail version of the images in a list (_preview.png)
- [x] When a thumbnail is tapped, present a detail view controller which will display all the images for that particular collection.