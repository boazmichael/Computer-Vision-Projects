# Computer Vision Using YOLO11n  

## Introduction:  
This is the README file for implementing jupyter notebook for computer vision using YOLO11n. The file contains all information on how to install a virtual environment for YOLO, and the setup and installations needed for all basic requirements. To the end the folder structure will also be referred. The notebook can be found by the name "Object_detection_work.ipynb".

## The Complete Installation guide

### Create the environment named 'yolo_env'
  python -m venv yolo_env

### Activate it:
  (On Windows): yolo_env\Scripts\activate
  (On macOS/Linux): source yolo_env/bin/activate  
  
### Install PyTorch  
  pip install torch torchvision torchaudio  
  
### Connect the Environment to Jupyter  
  pip install ipykernel
  python -m ipykernel install --user --name=yolo_env --display-name "Python (YOLO)"  
  
### Ultralytics Installation:  
  !{sys.executable} -m pip install ultralytics (if you're running in the notebook cell)  
  pip install ultralytics (terminal-linux)

### Verify in Jupyter Notebook  
  In the top right corner, click on the kernel name (usually "Python 3") and change it to "Python (YOLO)":  
  In the cell Run:  
  import torch  
  
  Check if PyTorch is installed  
  print(f"PyTorch Version: {torch.__version__}")  
  
  Check if your GPU is being detected (optional)  
  print(f"Is GPU available? {torch.cuda.is_available()}")  
  
## If Jupyter Notebook not installed:  
  pip install notebook  
  jupyter notebook (to launch it)  
  
## Annotation: 
There are multiple tools that you can use to annotate: RoboFlow, CVAT, MakeSense.AI  
For the task MakeSense was used though you may use any of your preference, and then export to YOLO format  

## The Dataset structure:  
  your_datset:  
  >dataset:
  >>train:  
  >>>images  
  >>>>frsme_01.jpeg  
  >>>>..
  <labels:  
  >>>>frame_01.txt  
  >>>>..
  >>val:  
  >>>images:  
  >>>>frsme_12.jpeg  
  >>>>..
  >>>labels:  
  >>>>frsme_12.txt  
  >>>>..
  >dataset.yaml  
