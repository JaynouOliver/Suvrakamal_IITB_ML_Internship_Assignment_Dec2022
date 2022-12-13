## Cricket ball release detection using ImageAI

### Detection used 

The results will showing the frame where ball leaves the hand of the person. 

```
git clone https://github.com/JaynouOliver/Suvrakamal_IITB_ML_Internship_Assignment_Dec2022
cd cricket_video_analysis 
pip install - r requirements.txt

```

download the pre-trained model from [here](https://github.com/OlafenwaMoses/ImageAI/blob/master/imageai/Detection/VIDEO.md#videodetection)

Keep the weights in te checkpoints folder and video in the data folder 


## Results from the tensorflow model 

Use the interference file to get the results from the models of tensorflow model.
You can try several different configs available [here](https://github.com/tensorflow/models/tree/master/research/object_detection/configs/tf2)

## Image_AI results 

```
cd src
python image_ai_interference.py

```

image_ai_inference.py to get the json for the cooridinate
results will be saved in the results dir
after that to get the frame where ball leaves the person.

```
python generate_results.py
```

To get the final output I am calculating euclidian distence between person and ball.


```
dst = math.sqrt((x1-x2)**2+(y1-y2)**2)

```
