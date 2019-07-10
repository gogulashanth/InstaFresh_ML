# InstaFresh_ML
TensorFlow Object Detection scripts used to create ML model for InstaFresh App

Dataset_creator.ipynb: This notebook is used to create the training and testing datasets in .tfrecord file format specifically
for Tensorflow object detection api. 

	INPUT: The input is a text file that has the list of classes in your dataset and a 
	set of images for your dataset saved in the same directory structure as output by OIDv4_Toolkit. The sript takes care of 
	creating the label maps and parsing the text files containing the bounding box info to create the record files.

	OUTPUT: The script outputs train.record, test.record and labelmap.pbtxt to be used for training.
	
ml_trainer.ipynb: This notebook performs the actual training and evaluation of the model. The notebook is designed to be run
on a colab environment (handles performing the necessary installs and downloading datasets, etc.)

	INPUT: The input is pointers to the train.record, test.record and labelmap.pbtxt. 
	
	OUTPUT: The script outputs several info regarding the model. (checkpoints, saved_models, tflite graph, etc.). Please
	refer to the code to customize the outputs.
