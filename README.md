# NSFW Art Classifier using CNN

### Disclaimer!

I used a web scraper to get all the images I use in this project. I do not recommend saving the images one by one. I would like to clarify that I did **NOT** view 1000+ lewd images.  

Since the dataset is a bit *uhh* crude *coughs*. I won't include them here. But if you want to try building a better model by optimizing the dataset, I'll gladly walk you through. First, create a new directory in the root folder `/data`. Then, create two more directories inside it and name them `nsfw` and `sfw` respectively. Finally, place the images inside those folders - unsafe works inside `data/nsfw` and safe works inside `data/sfw`. If you change the naming of the files, you will have to change some stuffs inside the `ai.ipynb` so I would not recommend but it is up to you. 

> You can create a new directory using `mkdir` in the command line

### About the Model

The model is made using Convolutional Neural Network (CNN) image classification. To optimize the prediction, I used MobileNetV2 transfer learning but I did some trial and errors for the hidden layers which you can see being commented out in `ai.ipynb`. 

Currently, the model has an accuracy of around 85-90%. The reason for this is probably because there are some arts that are borderline NSFW but not exactly NSFW, which the model may predict as either Safe or Not Safe. At the end of the day, the definitions of Safe and Not Safe varies with people. 

### Using the Model

To use the model, you can paste this snippet (and don't forget to install the correct dependencies).
```py
from tensorflow.keras.models import load_model

model = load_model(os.path.join('models/peko.tflite/'))
```

For implementations on using the model, you can refer to `test_model.ipynb`. There are 3 models so far in `/models/[*].tflite` but you can just use `peko.tflite`. 

### Demo
#### SFW
<img src="https://user-images.githubusercontent.com/83194022/216754762-f753e4b1-36c2-44ff-840b-512066ea19b6.png" width="200" height="auto">
#### NSFW
No. I can't publish.

> Created by Joshua James in 2023
