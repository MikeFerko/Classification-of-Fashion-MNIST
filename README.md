<!-- 4. Classification of MNIST Fashion Data set -->
<summary>4. Classification of Fashion MNIST Image Data Set</summary>     
<p>
  <ul>
    <li>Google Coolab Notebook: <a href="https://drive.google.com/file/d/197UP-kVRMQzCfOPd9AiP7Z4qxwMn9O54/view?usp=sharing">Jupyter Notebook</a></li>
    <li>Github Repository: <a href="https://github.com/MikeFerko/Classification-of-Fashion-MNIST">Respository</a></li>
    <li>Paper: <a href="https://github.com/MikeFerko/Classification-of-Fashion-MNIST/blob/main/Lab%202%20MNIST-Fashion%20Assignment_Michael%20Ferko.pdf">Classification of Fashion MNIST Image Data Set</a></li>
    <li>Categorical Cross Entropy Algorithm:</li>
    <ol type="1">
      <li>Load the Modified National Institute of Standards and Technology (MNIST) Fashion data set</li>
      <li>Train/Test split the data at a ratio of 6:1, respectively</li>
      <li>Reshape the images from 28x28 pixels to 784x1 pixels</li>
      <li>Normalise the image pixels by dividing by the gray scale image intensity level set L:</li>
      <p align="center">
       <a href="https://drive.google.com/file/d/197UP-kVRMQzCfOPd9AiP7Z4qxwMn9O54/view?usp=sharing">
       <img src="https://latex.codecogs.com/gif.latex?L%3D%5B0%2C2%5E%7Bk%7D-1%5D%3B%20k%3D8%20%5Crightarrow%20L%3D%5B0%2C255%5D%3B" width="35%" height="35%"></img>
       </a>
      </p>
      <li>Create 10 Categories for class_names = ['T-shirt/top', 'Trouser', 'Pullover', 'Dress', 'Coat',
               'Sandal', 'Shirt', 'Sneaker', 'Bag', 'Ankle boot']</li>
      <br></br>
      <p align="center">
        <a href="https://drive.google.com/file/d/197UP-kVRMQzCfOPd9AiP7Z4qxwMn9O54/view?usp=sharing"><img src="https://github.com/MikeFerko/Classification-of-Fashion-MNIST/blob/main/Fashion-MNIST-Dataset-GrayScale.png" width="50%" height="50%"></img>
        </a>
        <br>Creating 10 classes for the 10 types of clothing in the Image Data Set</br>
      </p>
      <br></br>
      <li>Categorical Cross Entropy (CE) Model Parameters:</li>
          <ul>
            <li><a href="https://en.wikipedia.org/wiki/Cross_entropy">categorical cross entropy (CE) Loss Function: </a></li>
            <p align="center">
            <a href="https://drive.google.com/file/d/197UP-kVRMQzCfOPd9AiP7Z4qxwMn9O54/view?usp=sharing">
            <img src="https://latex.codecogs.com/gif.latex?CE%20%3D%20-%5Csum_%7Bi%7D%5E%7BC%7Dt_%7Bi%7Dln%28s_%7Bi%7D%29" width="25%" height="25%"></img>
            </a>
            <br>Where: The formula can be seen as above, where  ti  refers to the  i -th element of the target vector and  si  refers to the  i -th element of the models output vector, and C the number of classes.</br>
            </p>
            <p align="center">
            <a href="https://drive.google.com/file/d/197UP-kVRMQzCfOPd9AiP7Z4qxwMn9O54/view?usp=sharing">
            <img src="https://github.com/MikeFerko/MikeFerko/blob/main/images/logLossCrossEntropy.png" width="75%" height="75%"></img>
            </a>
            <br>Visualization of Log Loss (Cross Entropy)</br>
            </p>
            <p align="center">
            <a href="https://drive.google.com/file/d/197UP-kVRMQzCfOPd9AiP7Z4qxwMn9O54/view?usp=sharing">
            <img src="https://github.com/MikeFerko/Classification-of-MNIST-70k-Handwritten-Digits-0-9-Image-Data-Set/blob/main/LAB-2-Fig2.png" width="50%" height="50%"></img>
            </a>
            <br>Cross Entropy between probability distributions for each Class</br>
            </p>
            <li><a href="https://www.tensorflow.org/api_docs/python/tf/keras/metrics/Accuracy">Model Accuracy: </a></li>
            <p align="center">
            <a href="https://drive.google.com/file/d/197UP-kVRMQzCfOPd9AiP7Z4qxwMn9O54/view?usp=sharing">
            <img src="https://latex.codecogs.com/gif.latex?Acc%3D%5Cfrac%7B1%7D%7BM%7D%5Csum_%7Bk%7D%5E%7BM%7Dargmax%28t_%7Bk%7D%29%20%3D%3D%20argmax%28s_%7Bk%7D%29" width="35%" height="35%"></img>
            </a>
            <br>Where: M is the number of samples in the dataset, tk is the target vector for the k-th sample, and sk is the models output vector for the k-th sample.</br>
            </p>
            <li>Neural Network Architecture:</li>
            <ul>
              <li>Input Layer = 64 ReLu activation neurons with an input shape of 784x1</li>
              <li>Hidden Layer = 64 ReLu activation neurons with an input shape of 64x1</li>
              <li>Output Layer = 10 softmax neurons</li>
              <p align="center">
              <a href="https://drive.google.com/file/d/197UP-kVRMQzCfOPd9AiP7Z4qxwMn9O54/view?usp=sharing">
              <img src="https://github.com/MikeFerko/Classification-of-Fashion-MNIST/blob/main/Fashion-MNIST-Neural-Network-Architecture.png" width="75%" height="75%"></img>
              </a>
              <br>Classification Neural Network Architecture</br>
              </p>
            </ul>
            <li><a href="https://en.wikipedia.org/wiki/Stochastic_gradient_descent">Stochastic Gradient Descent optimizer</a></li>
            <ul>
              <li>Learing Rate = 0.1</li>
              <li>Exponential Decay Factor = 0</li>
              <li>Momentum = 0</li>
            </ul>
            <li>Train Duration: 10 Epochs</li>
            <li>Batch Size = 128</li>
            <li>training samples = 60,000</li>
            <li>testing samples = 10,000</li>  
          </ul>
  </ul>
</p>
<br>7. Show Results: </br>
<p align="center">

<a href="https://drive.google.com/file/d/197UP-kVRMQzCfOPd9AiP7Z4qxwMn9O54/view?usp=sharing">
<img src="https://github.com/MikeFerko/Classification-of-Fashion-MNIST/blob/main/Fashipn-MNIST-Training.png" width="50%" height="50%"></img>
</a>
<br>Visualization of Model Loss and Accuracy (0.3090 and 88.66% Respectively)</br>
</p>

<p align="center">
<a href="https://drive.google.com/file/d/197UP-kVRMQzCfOPd9AiP7Z4qxwMn9O54/view?usp=sharing">
<img src="https://github.com/MikeFerko/Classification-of-Fashion-MNIST/blob/main/Fashion-MNIST-FirstLayerWeightVisualization.png" width="50%" height="50%"></img>
</a>
<br>Visualization of First Layer Weights W1 from Neural Network Architecture</br>
</p>

<p align="center">
<a href="https://drive.google.com/file/d/197UP-kVRMQzCfOPd9AiP7Z4qxwMn9O54/view?usp=sharing">
<img src="https://github.com/MikeFerko/Classification-of-Fashion-MNIST/blob/main/Fashion-MNIST-SecondLayerWeightVisualization.png" width="50%" height="50%"></img>
</a>
<br>Visualization of Second Layer Weights W2 from Neural Network Architecture</br>
</p>

<p align="center">
<a href="https://drive.google.com/file/d/197UP-kVRMQzCfOPd9AiP7Z4qxwMn9O54/view?usp=sharing">
<img src="https://github.com/MikeFerko/Classification-of-Fashion-MNIST/blob/main/Fashion-MNIST-ThirdLayerWeightVisualization.png" width="50%" height="50%"></img>
</a>
<br>Visualization of Third Layer Weights W3 from Neural Network Architecture</br>
</p>
