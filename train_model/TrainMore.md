# Adding More Classes to the Model

To add more classes to the model, follow these steps:

1. In the `capture_imgs.py` file, increase the `number_of_classes` variable to the desired number of new classes that you want to add. This variable controls how many classes the model will recognize.

2. Run the `capture_imgs.py` script. For each new class, press 'q' to signal the script to capture images for the new class. Capture several images from different angles and lighting conditions.

3. After capturing images for all the new classes, update the `labels_dict` variable in the `inference_classifier.py` file. Add entries for the new classes and ensure that they match the labels used when capturing the images.

4. Delete the following files and folders to start fresh:

   - `data.pickle`: This file contains the dataset information.
   - `model.p`: The pre-trained model.
   - The `data` folder: This contains the images used for training.

5. Once you've completed the steps above, proceed with the following sequence of scripts to train and use the model:

   - Run `collect_imgs.py` to organize the captured images into the appropriate folder structure.
   - Execute `create_dataset.py` to create a dataset from the collected images.
   - Run `train_classifier.py` to train the model on the updated dataset.
   - Finally, you are ready to run the main file, `inference_classifier.py`, which will use the trained model to recognize the added classes.

By following these steps, you can expand the capabilities of the model to recognize new ASL characters or classes effectively.
