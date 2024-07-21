# ***Train dataset***

----------------------------------------------------

Train dataset contain data for training YOLO model.

Each sample has two files (*.jpg, *.txt)

[Face Mask Detection - OpenCV University dataset](https://www.kaggle.com/datasets/radimkzl/face-mask-detection-opencv-university-dataset)

```Python
# Path to the directory for download
DIRECTORY_PATH = '<path_to_the_your_directory>'

# Download file of train dataset for YOLO
url_dataset = "https://storage.googleapis.com/kaggle-data-sets/5418712/8996055/bundle/archive.zip?X-Goog-Algorithm=GOOG4-RSA-SHA256&X-Goog-Credential=gcp-kaggle-com%40kaggle-161607.iam.gserviceaccount.com%2F20240721%2Fauto%2Fstorage%2Fgoog4_request&X-Goog-Date=20240721T120618Z&X-Goog-Expires=259200&X-Goog-SignedHeaders=host&X-Goog-Signature=841b24e49ffb7a7e6fd146d00b47f4a2c97de9fd0b550e50682ceed467ca27d231717db8adb3047b3252a4fc6f12b6c2e2e8876de95d11f0e7b236bfafdc8e9385497e14ae8e12d48285cdd78bebd434a6da53d0fc851cef937af52cab85894f201113ac52d7feda1196dc092e423702bb674f0bb834312aff08b6b5893d1aa6c6602174b6598b790b50731e8258f90733346c23eec15131dfc174e53561352290cb0b93ed550a13ed1b21172d016729b7a4322080fa4367e5dfbf316db2f065127d611c72c07e769002833c6aaeccb8acf1eb26ba02102f9e39404f1bb0a61d2530e4379a4f5103aa1ae969679f2e13e140a5ef1792700f19a9a458e300a6ce"
response_dataset = requests.get(url_dataset)
zip_file_dataset = zipfile.ZipFile(io.BytesIO(response_dataset.content))

# Unpack file
zip_file_dataset.extractall(os.path.join(DIRECTORY_PATH,"train_dataset"))
```