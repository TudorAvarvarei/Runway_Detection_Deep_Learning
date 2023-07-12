# Runway_Detection_Deep_Learning

This project consisted in a 5 months internship at ONERA that focused on training some pre-trained models on detecting and segmenting runways in images. It consists of the following folders:
- datasets: where training and testing dataset have to be sent in 3 folders (images, Annotations (for the training or testing of the RCNN model) and labels (for the training or testing of the YOLO model). It can contain multiple folders for training / testing
- models: where the models to be compared can be placed; the models require to be a Pytorch / YOLO model and they can be saved either as a whole model or as a dictionary
- bag_process: where a ROS bag can be given and, out of it, the images and its labels can be extracted (as Faster-RCNN labels)
- RCNN_to_YOLO: this code required the Annotations folder path and will transform all the labels inside in YOLO labels format inside a new folder called "labels"
- table_creator: where the results of comparison between models can be made; it requires testing dataset and the name of the models to looks for in the "models" folder
- train_RCNN: Folder used for training a Faster-RCNN model; it requires the dataset to be separated into Annotations and images
- train_YOLO: folder used for training a YOLO model; it requires a dataset.yaml file as explained on the YOLO website to run a YOLO model that will send to the location where the labels and images can be found;
