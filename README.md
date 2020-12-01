## 使用mtcnn对人脸数据进行对齐

#### **如果本项目对你 使用mtcnn对人脸数据进行对齐 有帮助. 欢迎Start...**

#### 环境安装

```
conda install tensorflow-gpu==1.9.0
conda install twisted
conda install scipy
conda install pillow
conda install scikit-learn
conda install requests
pip install opencv-python
```

#### 预训练模型 LFW训练集数据下载

[LFW数据集](http://vis-www.cs.umass.edu/lfw/lfw.tgz)

#### 运行人脸对齐

--image_size 留有裁剪人脸的余量

```
export PYTHONPATH=$(pwd)
python align_dataset_mtcnn.py ./data/input_data ./data/output_data --image_size 182 --margin 44
```

人脸对齐前: 

![Aaron_Patterson_0001](data/input_data/Aaron_Patterson/Aaron_Patterson_0001.jpg)

人脸对齐后: 

![Aaron_Patterson_0001](data/output_data/Aaron_Patterson/Aaron_Patterson_0001.png)

#### 对齐后的人脸数据有助于后续人脸 特征点检测, embedding等操作有较大的性能提升.

