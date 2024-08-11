# ***Notebooks***

> In the Jupyter Lab, Kaggle notebooks and Colab we train YOLO models an create base concept of use ONNX YOLO model.

### ***Train YOLO models***
-----------------------------------------

We train middle type of YOLOv10m, YOLOv9m, YOLOv8m, YOLOv6m, YOLOv5m, only YOLOv7 is base version.

- #### **YOLOv10m**
  - [GitHub - YOLOv10](https://github.com/THU-MIG/yolov10) 
  - [Colab notebook](https://github.com/RadimKozl/OpenCV_Project4/blob/main/notebooks/YOLOv10_FaceMaskDetection.ipynb)
- #### **YOLOv9m**
  - [GitHub - YOLOv9](https://github.com/WongKinYiu/yolov9)
  - [Colab notebook](https://github.com/RadimKozl/OpenCV_Project4/blob/main/notebooks/YOLOv9_FaceMaskDetection.ipynb)
- #### **YOLOv8m**
  - [GitHub - YOLOv8](https://github.com/autogyro/yolo-V8)
  - [GitHub - Ultralytics](https://github.com/ultralytics/ultralytics)
  - [Colab notebook](https://github.com/RadimKozl/OpenCV_Project4/blob/main/notebooks/YOLOv8_FaceMaskDetection.ipynb)
- #### **YOLOv7**
  - [GitHub - YOLOv7](https://github.com/WongKinYiu/yolov7)
  - [Kaggle notebook](https://github.com/RadimKozl/OpenCV_Project4/blob/main/notebooks/yolov7-facemaskdetection-kaggle.ipynb)
  - [Kaggle](https://www.kaggle.com/code/radimkzl/yolov7-facemaskdetection-kaggle)
- #### **YOLOv6m**
  - [GitHub - YOLOv6](https://github.com/meituan/YOLOv6)
  - [Kaggle notebook](https://github.com/RadimKozl/OpenCV_Project4/blob/main/notebooks/yolov6-facemaskdetection-kaggle.ipynb)
  - [Kaggle](https://www.kaggle.com/code/radimkzl/yolov6-facemaskdetection-kaggle)
- #### **YOLOv5m**
  - [GitHub - YOLOv5](https://github.com/ultralytics/yolov5)
  - [Colab notebook](https://github.com/RadimKozl/OpenCV_Project4/blob/main/notebooks/YOLOv5_FaceMaskDetection.ipynb)

Ve use two type of train of model, first we used Ultralytic libraries, second we used own GitHub project

### ***Test ONNX model on testing Images***
---------------------------------------------

We tested ONNX models by three types of possibilities.

- [***by Ultralytics library***](https://github.com/RadimKozl/OpenCV_Project4/blob/main/notebooks/onnx_model_YOLO_ultralitics.ipynb)
  
  This version is possible use only for model trained by Ultralytics library. (`YOLOv10m_FMD_01.onnx`, `YOLOv9m_FMD.onnx`, `YOLOv8m_FMD.onnx`, `YOLOv5m_FMD.onnx`) 

- [***by OpenCV library***](https://github.com/RadimKozl/OpenCV_Project4/blob/main/notebooks/onnx_model_YOLO_OpenCV.ipynb)
  
  There is use only 3 models for using, model `YOLOv10m_FMD_01` is not compatible with `dnn` of OpenCV. Models `YOLOv6_FMD_.onnx` and `YOLOv7_FMD_*.onnx`, have different output. We used only `YOLOv9m_FMD.onnx`, `YOLOv8m_FMD.onnx`, `YOLOv5m_FMD.onnx`.

- [***by Onnx-runtime library***](https://github.com/RadimKozl/OpenCV_Project4/blob/main/notebooks/onnx_model_YOLO_onnxruntime.ipynb)

  There is possible tested all models, only model `YOLOv7_FMD_02.onnx` is false type of model, it is not object detection model, see [models detail](https://github.com/RadimKozl/OpenCV_Project4/blob/main/notebooks/description_of_onnx_model_YOLO.ipynb).

[Show results](https://github.com/RadimKozl/OpenCV_Project4/tree/main/data/images/results)

### ***Test ONNX/Pt models on testing Videos***
-----------------------------------------------

- [***by Ultralytics & Roboflow supervision libraries***](https://github.com/RadimKozl/OpenCV_Project4/blob/main/notebooks/video-detection-yolo-roboflow-kaggle.ipynb)   [(Kaggle Version)](https://www.kaggle.com/code/radimkzl/video-detection-yolo-roboflow-kaggle)
  
  We used *.pt files, only models trained by the Ultralytics library, for compatibility with the libraries.
  (`YOLOv10m_FMD.pt`, `YOLOv9m_FMD.pt`, `YOLOv8m_FMD.pt`, `YOLOv5m_FMD.pt`)

- [***by OpenCV & ONNX-runtime libraries***](https://github.com/RadimKozl/OpenCV_Project4/blob/main/notebooks/video-detection-yolo-onnx_runtime.ipynb)

  We use the correct models `YOLOv9m_FMD.onnx`, `YOLOv8m_FMD.onnx`, `YOLOv5_FMD.onnx` with treshods 0.5 and 0.7. For more better results it will be neccesary change this values.

[Show results](https://github.com/RadimKozl/OpenCV_Project4/tree/main/data/videos/results)