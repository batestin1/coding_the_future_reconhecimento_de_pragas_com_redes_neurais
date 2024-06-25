<h1 align="center">
<img src="https://img.shields.io/static/v1?label=Teachable%20Machine%20POR&message=MAYCON%20BATESTIN&color=7159c1&style=flat-square&logo=ghost"/>

<h3> <p align="center">Teachnable Machine</p> </h3>
<h3> <p align="center"> ================= </p> </h3>



--- 
# Teachnable Machine

<p> Teachnable Machine é uma plataforma Low Code que permite teinar um computador para reconhecer suas próprias imagens, sons e poses.
Uma maneira rápida e fácil de criar modelos de aprendizado de máquina para seus sites, aplicativos e muito mais, sem necessidade de conhecimento ou codificação. </p>

1. Neste repositório você vai encontrar um diretório chamado `converted_keras` que contem o nosso modelo treinado 
2. Para usar o nosso projeto, baixe o arquivo `.tm` deste diretório [PROJETO](https://drive.google.com/file/d/1XOLU1J9xffvbuiKoYDefrq3T4lTAmESB/view?usp=sharing) acesse o link [LINK](https://teachablemachine.withgoogle.com/train) e importe o arquivo com a extensao `.tm`
3. Para usar o modelo realize o código abaixo:

```

from keras.models import load_model  # TensorFlow is required for Keras to work
from PIL import Image, ImageOps  # Install pillow instead of PIL
import numpy as np

# Disable scientific notation for clarity
np.set_printoptions(suppress=True)

# Load the model
model = load_model("keras_Model.h5", compile=False)

# Load the labels
class_names = open("labels.txt", "r").readlines()

# Create the array of the right shape to feed into the keras model
# The 'length' or number of images you can put into the array is
# determined by the first position in the shape tuple, in this case 1
data = np.ndarray(shape=(1, 224, 224, 3), dtype=np.float32)

# Replace this with the path to your image
image = Image.open("<IMAGE_PATH>").convert("RGB")

# resizing the image to be at least 224x224 and then cropping from the center
size = (224, 224)
image = ImageOps.fit(image, size, Image.Resampling.LANCZOS)

# turn the image into a numpy array
image_array = np.asarray(image)

# Normalize the image
normalized_image_array = (image_array.astype(np.float32) / 127.5) - 1

# Load the image into the array
data[0] = normalized_image_array

# Predicts the model
prediction = model.predict(data)
index = np.argmax(prediction)
class_name = class_names[index]
confidence_score = prediction[0][index]

# Print prediction and confidence score
print("Class:", class_name[2:], end="")
print("Confidence Score:", confidence_score)


````
