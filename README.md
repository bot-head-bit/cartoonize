# Cartoonizer

> Convert images and videos into a cartoon


## Installation

### Application tested on:

- python 3.7
- tensorflow 2.1.0 
- tf_slim 1.1.0
- ffmpeg 3.4.8
- Cuda version 10.1
- OS: Linux (Ubuntu 18.04)

### Using Docker

The easiest way to get the webapp running is by using the Dockerfile:

1. `cd` into the root directory and build the image
```
docker build -t cartoonize .
```
**Note**: Set the appropriate values in `config.yaml` before building the image.

2. Run the container by exposing the appropriate ports
```
docker run -p 8080:8080 cartoonize
```


### Using `virtualenv`

1. Make a virtual environment using `virutalenv` and activate it
```
virtualenv -p python3 cartoonize
source cartoonize/bin/activate
```
2. Install python dependencies
```
pip install -r requirements.txt
```
3. Run the webapp. Be sure to set the appropriate values in `config.yaml` file before running the application.
```
python app.py
```

### Using [Google Colab]
1. Clone the repository using either of the below mentioned way:
   - Using Command:
        - Create a new Notebook in Colab and in the cell execute the below command.  
        
        ```
         ! git clone https://github.com/bot-head-bit/cartoonize.git
        ```
        **Note:** Don't forget to add `!` at the beginning of the command
        
    - From Colab User Interface
 ```
        Open Colab
            └── File
                 └── Open Notebook
                          └── Github
                                └── paste the Url of the repository
 ```
 Note :  Before running the application change the runtime to GPU for processing videos but you for images CPU shall also work just fine.
 ```
            Runtime
               └── Change runtime type
                           └── Select GPU
 ```
2. After cloning the repository navigate to the `/cartoonize` using below command in the notebook cell:

   ```
   %cd cartoonize
   ```
3. Run the below commands in the notebook cell to install the requirements. 

   ```
   !pip install -r requirements.txt
   ```


4. In config.yaml file set: 

   ``` 
   colab-mode: true 
   ``` 
   
5. Launch the flask app on ngrok

   ```
   !python app.py
   ```


## Sample Image and Video

### Emma Watson Cartoonized
<img alt="Emma Watson Cartoonized" style="border-width:0" src="static/sample_images/twitter_image.png" />

### Youtube Video of Avenger's Bar Scene Cartoonized
[![Cartoonized version of Avenger's bar scene](http://img.youtube.com/vi/GqduSLcmhto/0.jpg)](http://www.youtube.com/watch?v=GqduSLcmhto "AVENGERS BAR SCENE [Cartoonized Version]")

---

## License

Copyright (C) Xinrui Wang, Jinze Yu. ([White box cartoonization](https://github.com/SystemErrorWang/White-box-Cartoonization))
    - All rights reserved. 
    - Licensed under the CC BY-NC-SA 4.0 
    - Also, Commercial application is prohibited license (https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode).
