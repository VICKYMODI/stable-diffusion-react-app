**to run stable diffusion webUi as an API server, follow this step -**

#create python virtual environment
#install requirement file to install necessary dependencies 
#finally run - **python3 launch.py --nowebui --skip-torch-cuda-test**
#This cmd will run stable diffusion web ui at port 7861 running on localhost - https://127.0.0.1:7861
#the txtToImg api can be accessed through below endpoint - **sdapi/v1/txt2img**
#the payload will be like this -

{
  "prompt": **userPromptGoesHere**,
  "steps": 50,
  "cfg_scale": 7.5
}

#Please note, running like this will also allow access to fast api docs page
#we can access the api docs from this url - **http://0.0.0.0:7861/docs**


**On React side :**

#i have set up the proxy on package.json to allow cors policy
#Please run react app from **npm start** from termial to access ui and image generation APIs
#this simple react app has dashboard option as well which will show the the previous prompt and images as well(only for current user)
