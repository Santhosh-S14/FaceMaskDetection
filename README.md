# AI Face Mask Detector

### Required Libraries
- PyTorch
- Sci-kit Learn
- Matplotlib
- PIL

Full Dataset: https://drive.google.com/drive/folders/1SicMq7uXRHL-SdyA6XnYVJy24yeQObkj?usp=sharing


### Classes, functions and their purpose:

1. get_images(image path, test_split) - to get the images and split the data into training, testing images and plotting the no.of images in each class.
2. Class model - Model for CNN with hidden layes and fully connected layers. 
3. Class ModelTraining - It takes model, device, optimizer and criterion as constructor arguments. Class also contains a training function to train the model with mentioned epochs. 
4. getModelAccuracy(model, test_dataloader, device) - get accuracy, classfication_report and confusion matrix on the test images. 
5. predict_image(model, image, device, labels) - To predict a single image on the trained model. 

### Working of the project:

#### To load dataset and train model

1. To load the dataset call the get_images function with the parameters: image_path and test_split based on your requirements.
2. To train the model 
    1. Create object of Model class
    3. Use the object created for CNN model and call training function inside the ModelTraining class

This will save the trained model in the model_path.  

#### Testing and Evaluation

For testing and evaluating the model
1. Call getModelAccuracy function with created model from above, test_loader and device. This gives you test accuracy, classfication report and confusion matrix. 
2. To evaluate model on single image call predict_image with saved model, image path on which you want to predict the class and device. 

