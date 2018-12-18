# Config

##Project

All global project configurations are stored in `config/project.yaml`.

####name

Specify the name of your project.

Example:
~~~yaml
name: "deeplodocus_project"
~~~

####cv_library

Specify the computer vision library with which to read and manipulate image or video files.

Example: 
~~~yaml
cv_library: 1
~~~

Valid entries with corresponding CV library are tabulated below:

| Entry  | Computer Vision Library |
| --- | --- |
| 0 | No CV Library |
| 1 | OpenCV |
| 2 | PIL  |

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
~~~



##Model

##Optimizer

##Metrics

##Training

##Data

##Transform

##History

##Losses