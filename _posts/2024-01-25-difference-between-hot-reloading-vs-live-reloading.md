--- 
layout: post
author: Shawn Phy
--- 

## What is hot reloading
Often during development of any python or react native application you might need to change multiple files and see the results instantly but you dont need to the entire application to reload. This can sometimes be time consuming and taxing on your machine. 

Enter `Hot reloading` this is a feature that allows developers to see changes made to files in real time. It eliminates the need to manually refresh the page furthermore, it preserves the state of the app. Any functions that were in use before the reload will be available after the reload. 

## what is live reloading
This is a feature that has been implemented in some [vs code extensions](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) it enables developers to see changes made to the code in real time but it reloads the entire application discarding the current state. If there are variables and components that were in use previously they will be discarded on the reload. This option is particularly useful when there are problems with the current state of the application. 

## Illustration 
if you have a python application that either uses [FastAPi](https://fastapi.tiangolo.com/), [flask](https://flask.palletsprojects.com/en/3.0.x/), we can use the python package `uvicorn` to do hot reloading 
```
uvicorn main:app --reload
```
In the above command `--reload` is used to indicate that the server should run a hot reload. 

If you need to do a live reload you could use the vs code extension. 

