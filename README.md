# ✨ Instance Segmentation using PixelLib 🙆‍♂️
A streamlit based webapp to perform SOTA instance segmentation on images, videos and live webcam feed

## Installation:
* Simply run the command ***pip install -r requirements.txt*** to install the necessary dependencies.
* In case you need to use your GPU for computation, ensure that you have the right CUDA drivers and CUDNN installed.

## Usage:
1. Simply run the command: 
```
streamlit run app.py
```
2. Navigate to http://localhost:8501 in your web-browser.
3. By default, streamlit allows us to upload files of **max. 200MB**. If you want to have more size for uploading audio files, execute the command :
```
streamlit run app.py --server.maxUploadSize=1028
```


------------
## Results 
------------

### Images
| **Original Image**  | **Segmented Image**  |
|---------------------|-----------------------|
| ![pic1](uploads/1.jpg)  | ![pic1](downloads/segmented_1.jpg)  |
| ![pic2](uploads/2.png)  | ![pic2](downloads/segmented_2.png)  |
| ![pic3](uploads/3.bmp)  | ![pic3](downloads/segmented_3.bmp)  |
| ![pic4](uploads/4.jpeg) | ![pic4](downloads/segmented_4.jpeg)  |
 

# Videos
| **Original Video**  | **Segmented Video**  |
|---------------------|-----------------------|
| ![pic1](gifs/1.gif)  | ![pic1](gifs/segmented_1.gif)  |
| ![pic2](gifs/2.gif)  | ![pic2](gifs/segmented_2.gif)  |
| ![pic3](gifs/3.gif)  | ![pic3](gifs/segmented_3.gif)  |

# Live Webcam Feed
***coming soon...***

### Running the Dockerized App
1. Ensure you have Docker Installed and Setup in your OS (Windows/Mac/Linux). For detailed Instructions, please refer [this.](https://docs.docker.com/engine/install/)
2. Navigate to the folder where you have cloned this repository ( where the ***Dockerfile*** is present ).
3. Build the Docker Image (don't forget the dot!! :smile: ): 
```
docker build -f Dockerfile -t app:latest .
```
4. Run the docker:
```
docker run -p 8501:8501 app:latest
```

This will launch the dockerized app. Navigate to ***http://localhost:8501/*** in your browser to have a look at your application. You can check the status of your all available running dockers by:
```
docker ps
```
