# Config

## Project

All global project configurations are stored in `config/project.yaml`.

Example:
~~~yaml
sub_project: "v01"
cv_library: "opencv"
device: "auto"
device_ids: "auto"
logs:
  history_train_batches: True
  history_train_epochs: True
  history_validation: True
  notification: True
on_wake: Null
~~~

#### sub_project

Specify the name of your current session.
Results from the current session, such as weights, logs and history will be saved into a sub-directory with this name.

- Data type: str
- Default value: "version01"

Example:
~~~yaml
name: "version01"
~~~

#### cv_library

Specify the computer vision library with which to read and manipulate image or video files.

- Data type: str
- Default value: "pil"
- Valid entries: 
    - "pil"
    - "opencv"
    
Use "pil" to specify the Python Imagin Library (a.k.a. PIL/Pillow) or "opencv" to specify the Open Source Computer Vision Library (OpenCV). 
(Note that OpenCV is typically ~ 50% faster.)

Example: 
~~~yaml
cv_library: "opencv"
~~~

#### device

Specify the device to use. 

- Data type: str
- Default value: "auto"
- Valid entries: 
    - "auto"
    - "cuda:0"
    - "cpu"

Example:
~~~yaml
device: "cuda:0"
~~~

The CPU or a CUDA device can be specified explicitly with "cpu" or "cuda:0" respectively. 
Or, if "auto" is given, the device will be set to "cuda:0" if available, otherwise "cpu".

#### device_ids

If using multiple GPUs, you may specify the specific devices to use. Alternatively, use "auto" to automatically find and use all available CUDA-enabled GPUs. 

- Data type: list of ints
- Default value: "auto"
- Valid entries: 

Example: 
~~~yaml
device_ids: [0, 1, 2]
~~~

#### logs

Specify whether or not to write each type of log file.

Example:
~~~yaml
logs:
  history_train_batches: True
  history_train_epochs: True
  history_validation: True
  notification: True
~~~

- `history_train_batches` - training history for each batch.
- `history_train_epochs` - training history for each epoch.
- `history_validation` - validation history.
- `notification` - log all inputs and outputs of the deeplodocus interface.

#### on_wake

Specify any start-up commands.

Example: 
~~~yaml
on_wake:
  - config.summary()
  - load()
  - train()
  - sleep()
~~~



## Model

## Optimizer

## Metrics

## Training

## Data

## Transform

## History

## Losses