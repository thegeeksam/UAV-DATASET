# UAV-DATASET
This repository contains a dataset of images and videos captured by unmanned aerial vehicles (UAVs) in various scenarios and environments. The dataset can be used for research and development of computer vision and machine learning algorithms for UAV applications, such as object detection, tracking, segmentation, classification, etc.

The dataset consists of the following folders:

- Images: This folder contains 1000 high-resolution images (1920x1080) taken by UAVs in different settings, such as urban, rural, forest, desert, etc. The images are labeled with bounding boxes and class names for 10 common objects of interest, such as cars, pedestrians, buildings, trees, etc. The labels are stored in XML files following the PASCAL VOC format.
- Videos: This folder contains 100 video clips (30 fps) with variable durations (from 10 to 60 seconds) recorded by UAVs in various scenarios and environments. The videos are also labeled with bounding boxes and class names for the same 10 objects as the images. The labels are stored in CSV files following the MOTChallenge format.
- Splits: This folder contains text files that define the train, validation and test splits for the dataset. Each file lists the image or video names that belong to each split. The splits are designed to ensure a balanced distribution of objects and scenarios across the splits.

## How to use the dataset
To use the dataset, you need to clone this repository or download it as a zip file. You can then access the images, videos and labels from the respective folders. You can also use the provided scripts to load and visualize the data in Python.

- To load an image and its labels, you can use the `load_image` function from the `utils.py` script. This function takes an image name as input and returns a PIL image object and a list of dictionaries containing the label information for each object in the image. Each dictionary has the following keys: 'name', 'xmin', 'ymin', 'xmax', 'ymax'.
- To load a video and its labels, you can use the `load_video` function from the `utils.py` script. This function takes a video name as input and returns a cv2 video capture object and a pandas dataframe containing the label information for each frame and object in the video. The dataframe has the following columns: 'frame', 'id', 'name', 'xmin', 'ymin', 'xmax', 'ymax'.
- To visualize an image or a video with its labels, you can use the `show_image` or `show_video` functions from the `utils.py` script. These functions take an image or a video object and its labels as input and display them using matplotlib.

## Citation
If you use this dataset in your research, please cite the following paper:
S. Sampathkumar & R. Rajeswari (2022) An Automated Crop and Plant Disease Identification Scheme Using Cognitive Fuzzy C-Means Algorithm, IETE Journal of Research, 68:5, 3786-3797, DOI: 10.1080/03772063.2020.1780163
