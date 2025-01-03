
# MS-MD-YOLO  

![License](https://img.shields.io/github/license/ELF233/MS-MD-YOLO)  
![Stars](https://img.shields.io/github/stars/ELF233/MS-MD-YOLO)  
![Issues](https://img.shields.io/github/issues/ELF233/MS-MD-YOLO)  

**MS-MD-YOLO** 是一个基于 YOLO 的多尺度、多方向的目标检测模型，旨在提升目标检测的精度和效率。  

---  

## 📖 目录  

1. [项目简介](#项目简介)  
2. [功能特性](#功能特性)  
3. [安装与使用](#安装与使用)  
   - [环境要求](#环境要求)  
   - [安装步骤](#安装步骤)  
   - [数据集配置](#数据集配置)  
   - [训练模型](#训练模型)  
   - [测试模型](#测试模型)  
4. [联系信息](#联系信息)  

---  

## 项目简介  

**MS-MD-YOLO** 是一种基于 YOLOv7 的多方向多尺度局部特征增强红外目标检测方法，以应对红外成像技术在不同光照和天气条件下的独特优势。  

该模型的主要创新点包括：  
- **Mamba 模块**：通过选择机制和多尺度特征分支有效捕捉不同尺度的目标细节。  
- **S-ELAN 模块**：结合多方向扫描和深度卷积结构，增强多尺度特征提取。  
- **局部特征增强模块**：利用膨胀卷积扩展感受野，并通过 CBAM 注意机制改善特征表示，从而提升模型对目标的语义理解。  

实验结果表明，该模型在自构建的多尺度红外目标数据集上表现出色，并在 FLIR 公共数据集上优于现有最先进的方法，显示出其在红外目标检测中的有效性和强泛化能力。  

---  

## ✨ 功能特性  

- ✅ 支持多尺度目标检测  
- ✅ 集成 Mamba 特征提取模块  
- ✅ 高效的推理速度  
- ✅ 适用多种数据集  

---  

## 🚀 安装与使用  

### 环境要求  

以下是项目所需的完整依赖包列表：  

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

### 安装步骤  

1. **克隆项目到本地**：  

   ```bash  
   git clone https://github.com/ELF233/MS-MD-YOLO  
   cd MS-MD-YOLO

### 数据集配置  

1. 将数据集放置在 `data` 文件夹中。  
2. 修改 `data` 文件夹中的配置文件，调整数据集路径以匹配本地环境。  

---  

### 训练模型  

1. 打开 `train.py` 文件，根据需求设置训练参数（如批量大小、训练轮数等）。  
2. 运行以下命令开始训练：  

   ```bash  
   python train.py

### 测试模型  

1. 打开 `test.py` 文件，根据需求设置测试参数（如模型路径、测试数据路径等）。  
2. 运行以下命令进行测试：  

   ```bash  
   python test.py
##  📬 联系信息  

- **邮箱**：1499583398@qq.com  
- **代码仓库**：[MS-MD-YOLO on GitHub](https://github.com/ELF233/MS-MD-YOLO)
