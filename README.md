# ML_tf2_object_detection_nu
- This Tool help you train your object-detection model and convert to tflite-model which is easy to deploy on your device.
- The training framework is using Tensorflow object detection API on Tensoflow-2 & Tensorflow-1.
- The notebooks help you simplify the complicated installation steps and easy to use data preparing, training and converting. 
## First step
#### 1. Install anaconda
- Download the [anaconda](https://www.anaconda.com/products/distribution) and install it.
#### 2. Install the Visual C++ 2015 build tools
- Login https://my.visualstudio.com/Downloads （You will need a free Microsoft account）
- Enter `Build Tools` in search.
- Choose the left side `Visual Studio 2015 Update 3`.
- Choose `DVD` at `Visual C++ Build Tools . . .` and click download.
- Execute the install steps.
<img src="https://user-images.githubusercontent.com/105192502/209085872-18dadffb-aa0d-4c07-9780-f2a1237b2211.png" width="60%">

#### 3. Install [git windows version](https://gitforwindows.org/)
- Git is needed at the 5th step. 
#### 4. Download this git folder 
- `git clone https://github.com/OpenNuvoton/ML_tf2_object_detection_nu.git`
- Or you can download the zip file directly
#### 5. Python env create
- First use `create_conda_env_tf2.ipynb` to create the object-detection python running environment.
- Second, close and reopen Anaconda. Use `setup_objdet_tf2.ipynb` to install the remaining packages.
- [ Tf1 object detection ]: We also offer a Tf1 object detection env create, and please check `create_conda_env_tf1.ipynb` & `setup_objdet_tf1.ipynb`.
---
## Work Flow
<img src="https://user-images.githubusercontent.com/105192502/203241236-e6c729f4-8087-439c-9b0d-0fffbf602c71.png" width="80%">

## data prepare
- Open `create_data.ipynb` in `image_dataset`. This should be excuted in tf2 env (Check `create_conda_env_tf2.ipynb` & `setup_objdet_tf2.ipynb` to create tf2 env).
- This process will handle downloading open source images or labeling your customized images to create train dataset.
- The tutorial is in this notebook.

## train & tflite model creating
- open `workspace` folder.
- User need to choose tf1 or tf2 environment basing on user's training model.
- This process will handle training, mAP evaluation and converting tflite.
- The tutorial is in the notebook.

### tensorflow2
- `train_evl_monitor_tf2.ipynb` offers an easy UI to help user training, evaluation and monitoring.
- `convert_tflite_tf2.ipynb` offers an easy UI to help user converting tflite

[alternative way]:
- Open `train_cmd_tf2.ipynb`. This should be excuted in tf2 env.
- Google's object detection support models: [TensorFlow 2 Detection Model Zoo](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md) 

### tensorflow1
- Open `train_cmd_tf1.ipynb`. This should be excuted in tf1 env (Check `create_conda_env_tf1.ipynb` & `setup_objdet_tf1.ipynb` to create tf1 env).
- Google's object detection support models: [TensorFlow 1 Detection Model Zoo](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1_detection_zoo.md) 

## evaluation & test
- Open `test_tflite.ipynb` in `workspace`. This should be excuted in tf2 env.
- Examine/evaluation the result of tflite model with user's dataset. 
- The tutorial is in this notebook.
