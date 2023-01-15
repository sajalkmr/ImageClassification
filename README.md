

<h1>Image Classifier</h1>
<p>This project provides a script to train a convolutional neural network (CNN) on a dataset of images. The script is written in Python and uses TensorFlow and OpenCV. The model can classify images into different classes based on the dataset provided.</p>

<h2>Requirements</h2>
<ul>
  <li>Tensorflow</li>
  <li>Tensorflow-gpu</li>
  <li>OpenCV-python</li>
  <li>Matplotlib</li>
</ul>

<h2>Usage</h2>
<ol>
  <li>Clone or download the repository.</li>
  <li>Make sure that you have the required libraries installed.</li>
  <li>Place your dataset in a directory called 'training_data'</li>
  <li>Open the Jupyter notebook by running the command "jupyter notebook" in your terminal in the directory.</li>
  <li>Locate and open the training_model.ipynb notebook</li>

  <li>Make sure that the kernel for the notebook is set to Python 3.</li>
  <li>Run the cells in the notebook to train the model on your dataset.</li>
  <li>The script will create a unique folder with the current date and time in the format dd.mm.yyyy hhmmss-train_results for storing the model files and training results.</li>
  <li>To use this script, you will need to place your dataset of images in a directory called 'training_data'. The script expects the images to be organized into different subfolders within the 'training_data' directory, one for each class. For example, if you have two classes, "class1" and "class2", you should create two subfolders within the 'training_data' directory named "class1" and "class2" and place the corresponding images in each folder. Make sure that the images are in jpeg, jpg, bmp, or png format.</li>
  <br>
  </ol>
  <h2>Example file structure:</h2>
  <ol>
<pre>
training_data/
    class1/
        image1.jpg
        image2.jpg
        ...
    class2/
        image1.jpg
        image2.jpg
        ...
</pre>
</ol>

<h2>Model architecture</h2>
<p>The model architecture is a convolutional neural network (CNN) with the following layers:</p>
<ul>
  <li>Conv2D with 16 filters of size (3,3), stride of 1, and ReLU activation</li>
  <li>MaxPooling2D</li>
  <li>Conv2D with 32 filters of size (3,3), stride of 1, and ReLU activation</li>
  <li>MaxPooling2D</li>
  <li>Conv2D with 16 filters of size (3,3), stride of 1, and ReLU activation</li>
  <li>MaxPooling2D</li>
  <li>Flatten layer</li>
  <li>Dense layer with 128 units and ReLU activation</li>
  <li>Dense layer with the number of units equal to the number of classes in the dataset and softmax activation</li>
</ul>
<p>You can change the architecture of the model, training parameters, and data set path accordingly.</p>

  
<h2>Files saved after training</h2>
<p>The script will save the following files in the unique folder created after training:</p>
<ul>
  <li>The trained model file in the format model.h5</li>
  <li>A plot figure of a batch of the training images and their labels in the format batch_result.jpg</li>
  <li>An Accuracy and a Loss chart as accuracy_chart.jpg and loss_chart.jpg</li>
 
  <li>A file with the training and validation accuracy and loss values in the format histroy.json</li>
   <li>Final summary and result as .txt</li>
</ul>
  
 <h2>Training Results</h2>
<p>The following images are examples of the results generated by the script after training.</p>

<div>
    <img src="08.01.2023 221335-train_results/batch_result.jpg" width="23%" style="display:inline-block;">
    <img src="08.01.2023 221335-train_results/accuracy_chart.jpg" width="30%" style="display:inline-block;">
    <img src="08.01.2023 221335-train_results/loss_chart.jpg" width="30%" style="display:inline-block;">
</div>


  
</ol>

  
  
  
<h2>Note</h2>
<ul>
  <li>This script is set to work with images of size 256x256, you can change the image size accordingly.</li>
  <li>The script automatically loads the images and splits them into train, validation, and test sets.</li>
  

</ul>
  
  
<h2>Contributing</h2>
<p>If you want to contribute to this project, please feel free to submit a pull request.</p>
  
  
  
<h2>Licence</h2>
<p>This project is licensed under the MIT License - see the LICENSE.md file for details.</p>

<h2>References</h2>

  <p>The code for this project is greatly inspired by <a href="https://github.com/nicknochnack">Nicholas Renotte</a>.</p>



<h2>Examples</h2>
<p>You can find an example of a pre-trained model in the model folder, which was trained to classify images as notes and non-notes from WhatsApp images. You can use this pre-trained model as a starting point for fine-tuning on your own dataset or as a reference for comparison to your own model's performance. The model is trained using two classes (notes and non-notes) and the code is available in this repository <a href="https://github.com/sajalkmr/WhatsAppNotesSeparator">WhatsAppNotesSeparator</a>.</p>

