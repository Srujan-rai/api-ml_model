# Plant 🌱 Disease 🐛 Detector 🔎
 

## Machine Learning Model

Multi-Class Image classifier Built on PyTorch framework using CNN architecture. Currently Project Detects 17 States of disease in 4 plants ( Aiming Kerala State ) namely Cherry, Pepper, Potato and tomato.

* Framework : PyTorch
* Architecture : Convolutional Neural Networks
* Validation Accuracy : 77.7%



#### How to train

Upload the **[Python notebook](https://github.com/nandakishormpai2001/Plant_Disease_Detector/blob/main/model/Plant_Disease_Identifier.ipynb)** to Google Colab and run each cell for training the model. I have included a demo dataset to configure quickly. You can use this **[Kaggle Dataset](https://www.kaggle.com/vipoooool/new-plant-diseases-dataset)** which is the original one with huge amount of pictures.

#### How It Works

The input image dataset is converted to tensor and is passed through a CNN model, returning an output value corresponding to the plant disease. Input image tensor is passed through four convolutional layers and then flattened and inputted to fully connected layers.


#### API : How to use

API has been built on this classifier. URL = "https://plant-disease-detector-pytorch.herokuapp.com/"

User has to send a POST request to the given api with Base64 string of the Image to be input. 

```python
import requests
url = "https://plant-disease-detector-pytorch.herokuapp.com/"
#imgdata = base64 string of image
r = requests.post(url,json = {"image":imgdata})
print(r.text.strip())
```
Output
```python
'{"disease":"Septoria leaf spot","plant":"Tomato","remedy":"Remove infected leaves immediately,......Fungonil and Daconil)."}'
```

#### How to train

Upload the [Python notebook](https://github.com/nandakishormpai2001/Plant_Disease_Detector/blob/main/Plant_Disease_Identifier.ipynb) to Google Colab and run each cell for training the model. I have included a demo dataset to configure quickly. You can use this [Kaggle Dataset](https://www.kaggle.com/vipoooool/new-plant-diseases-dataset) which is the original one with huge amount of pictures.
