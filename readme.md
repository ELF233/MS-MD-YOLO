
# MS-MD-YOLO  

![License](https://img.shields.io/github/license/ELF233/MS-MD-YOLO)  
![Stars](https://img.shields.io/github/stars/ELF233/MS-MD-YOLO)  
![Issues](https://img.shields.io/github/issues/ELF233/MS-MD-YOLO)  

**MS-MD-YOLO** is a multi-scale, multi-directional object detection model based on YOLO, designed to improve the accuracy and efficiency of object detection.  

---  

## 📖 Table of Contents  

1. [Project Overview](#project-overview)  
2. [Features](#features)  
3. [Installation and Usage](#installation-and-usage)  
   - [Requirements](#requirements)  
   - [Installation Steps](#installation-steps)  
   - [Dataset Configuration](#dataset-configuration)  
   - [Training the Model](#training-the-model)  
   - [Testing the Model](#testing-the-model)  
4. [Contact Information](#contact-information)  

---  

## Project Overview  

**MS-MD-YOLO** is a multi-directional, multi-scale local feature enhancement infrared object detection method based on YOLOv7. It is designed to leverage the unique advantages of infrared imaging technology under various lighting and weather conditions.  

The main innovations of this model include:  
- **Mamba Module**: Effectively captures details of objects at different scales through a selection mechanism and multi-scale feature branches.  
- **S-ELAN Module**: Enhances multi-scale feature extraction by combining multi-directional scanning and deep convolutional structures.  
- **Local Feature Enhancement Module**: Expands the receptive field using dilated convolutions and improves feature representation through the CBAM attention mechanism, enhancing the model's semantic understanding of objects.  

Experimental results show that this model performs exceptionally well on a self-constructed multi-scale infrared object dataset and outperforms state-of-the-art methods on the FLIR public dataset, demonstrating its effectiveness and strong generalization ability in infrared object detection.  

---  

## ✨ Features  

- ✅ Supports multi-scale object detection  
- ✅ Integrated Mamba feature extraction module  
- ✅ High inference speed  
- ✅ Compatible with various datasets  

---  

## 🚀 Installation and Usage  

### Requirements  

Below is the complete list of dependencies required for the project:  

- absl-py==2.1.0  
- addict==2.4.0  
- aliyun-python-sdk-core==2.16.0  
- aliyun-python-sdk-kms==2.16.5  
- attrs==24.2.0  
- Automat==24.8.1  
- Brotli==1.0.9  
- buildtools==1.0.6  
- causal_conv1d==1.1.3  
- certifi==2024.8.30  
- cffi==1.17.1  
- chardet==5.2.0  
- charset-normalizer==3.3.2  
- click==8.1.7  
- cloudpickle==3.1.0  
- cmake==3.30.4  
- colorama==0.4.6  
- constantly==23.10.4  
- contourpy==1.3.0  
- crcmod==1.7  
- cryptography==43.0.3  
- cycler==0.12.1  
- docopt==0.6.2  
- einops==0.8.0  
- exceptiongroup==1.2.2  
- filelock==3.14.0  
- fonttools==4.54.1  
- fsspec==2024.9.0  
- furl==2.1.3  
- fvcore==0.1.5.post20221221  
- gmpy2==2.1.2  
- grad-cam==1.5.4  
- greenlet==3.1.1  
- grpcio==1.67.0  
- huggingface-hub==0.26.0  
- hyperlink==21.0.0  
- idna==3.7  
- importlib_metadata==8.5.0  
- incremental==24.7.2  
- iniconfig==2.0.0  
- iopath==0.1.10  
- Jinja2==3.1.4  
- jmespath==0.10.0  
- joblib==1.4.2  
- kiwisolver==1.4.7  
- mamba_ssm==1.1.3  
- Markdown==3.7  
- markdown-it-py==3.0.0  
- MarkupSafe==2.1.3  
- matplotlib==3.9.2  
- mdurl==0.1.2  
- mkl_fft==1.3.10  
- mkl_random==1.2.7  
- mkl-service==2.4.0  
- mmcv-full==1.7.2  
- model-index==0.1.11  
- mpmath==1.3.0  
- networkx==3.2.1  
- ninja==1.11.1.1  
- numpy==1.24.2  
- opencv-python==4.7.0.72  
- opendatalab==0.0.10  
- openmim==0.3.9  
- openxlab==0.1.2  
- ordered-set==4.1.0  
- orderedmultidict==1.0.1  
- oss2==2.17.0  
- packaging==24.1  
- pandas==2.2.3  
- pillow==10.4.0  
- pip==24.2  
- platformdirs==4.3.6  
- pluggy==1.5.0  
- portalocker==2.10.1  
- protobuf==5.28.2  
- pycocotools==2.0.8  
- pycparser==2.22  
- pycryptodome==3.21.0  
- Pygments==2.18.0  
- pyparsing==3.2.0  
- PySocks==1.7.1  
- pytest==8.3.3  
- python-dateutil==2.9.0.post0  
- pytz==2023.4  
- pywin32==308  
- PyYAML==6.0.2  
- redo==3.0.0  
- regex==2024.9.11  
- requests==2.28.2  
- rich==13.4.2  
- safetensors==0.4.5  
- scikit-learn==1.5.2  
- scipy==1.10.0  
- seaborn==0.13.2  
- selective_scan==0.0.2  
- setuptools==61.0.0  
- simplejson==3.19.3  
- six==1.16.0  
- SQLAlchemy==2.0.36  
- submitit==1.5.2  
- sympy==1.13.2  
- tabulate==0.9.0  
- tensorboard==2.18.0  
- tensorboard-data-server==0.7.2  
- tensorboardX==2.6.2.2  
- termcolor==2.5.0  
- threadpoolctl==3.5.0  
- timm==0.4.12  
- tokenizers==0.20.1  
- tomli==2.0.2  
- torch==2.2.2  
- torchaudio==2.2.2  
- torchvision==0.17.2  
- tqdm==4.65.2  
- transformers==4.45.2  
- triton==2.0.0  
- ttach==0.0.3  
- Twisted==24.7.0  
- typing_extensions==4.11.0  
- tzdata==2024.2  
- urllib3==1.26.20  
- Werkzeug==3.0.4  
- wheel==0.44.0  
- win-inet-pton==1.1.0  
- yacs==0.1.8  
- yapf==0.40.2  
- zipp==3.20.2  
- zope.interface==7.1.0  

### Installation Steps  

1. **Clone the repository to your local machine**:  

   ```bash  
   git clone https://github.com/ELF233/MS-MD-YOLO  
   cd MS-MD-YOLO
   ### Dataset Configuration  

1. Place your dataset in the `data` folder.  
2. Modify the configuration files in the `data` folder to match the dataset paths in your local environment.  

### Training the Model  

1. Open the `train.py` file and set the training parameters (e.g., batch size, number of epochs, etc.) as needed.  
2. Run the following command to start training:  

   ```bash  
   python train.py
   
### Testing the Model  

1. Open the `test.py` file and set the testing parameters (e.g., model path, test data path, etc.) as needed.  
2. Run the following command to start testing:  

   ```bash  
   python test.py
  
---  
## 📬 Contact Information

-   **Email**:  [1499583398@qq.com](mailto:1499583398@qq.com)
-   **Repository**:  [MS-MD-YOLO on GitHub](https://github.com/ELF233/MS-MD-YOLO)
