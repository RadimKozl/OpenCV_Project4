# ***Test dataset***

--------------------------------------------------------------------

Test dataset contain data for testing trained models.

There are:

- 4. images
- 2. videos

--------------------------------------------------------------------

Test dataset is upload on Kaggle:

[Face Mask Detection - OpenCV University dataset](https://www.kaggle.com/datasets/radimkzl/face-mask-detection-opencv-university-dataset)


```Python
# Path to the directory for download
DIRECTORY_PATH = '<path_to_the_your_directory>'

# Download file of test dataset for trained YOLO model
url_dataset = "https://storage.googleapis.com/kaggle-data-sets/5418979/8996440/bundle/archive.zip?X-Goog-Algorithm=GOOG4-RSA-SHA256&X-Goog-Credential=gcp-kaggle-com%40kaggle-161607.iam.gserviceaccount.com%2F20240721%2Fauto%2Fstorage%2Fgoog4_request&X-Goog-Date=20240721T121758Z&X-Goog-Expires=259200&X-Goog-SignedHeaders=host&X-Goog-Signature=80ece52746bf0228e28590aa13f6726eb1d63e18532a05c359d212c209be8d53bdd68361d91935f69fd63092fb576fd1bd667ae24bab77de71add224b8a9654564bc33c195ad42df9f25992e68e83677df22d3fb4e86e7c7ef92363cb244d7e3c68cde895be8a0162e70bf1117b7a65c2338556250a27092399aa05a1484e43b63c8c197c0e32d6c454af3dbb1f7512d2367254d85c7b4c94ed9ce54e51f6414271c04277a9c3039f2d0ecac8879bbb61f934ca5d965b5deda8bcca57e7b9710a9570732d73d79592672644599ed5fe1e3bd899b5b15838aecfda18e7e30ba57a22d27d58c2759269c57a99ae7ea3ed38199948c8d4100d0fa5c95273e0058d6"
response_dataset = requests.get(url_dataset)
zip_file_dataset = zipfile.ZipFile(io.BytesIO(response_dataset.content))

# Unpack file
zip_file_dataset.extractall(os.path.join(DIRECTORY_PATH,"test_dataset"))
```
