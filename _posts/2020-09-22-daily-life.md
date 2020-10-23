---
layout: post
title: "20200922"
date: 2020-09-22 12:44:56 +0800
comments: true
author:     CodingDonkey
categories: [php,每天写一点]
---

openmp paralle
  just partition the image into strip
  each thread compute each strip by it self
  need to seqentilise it together?
最近研究了如何通过 怎么 这两个词进行拓展，搜集词条库，再进行分词，排序，归类，对于以后的需求挖掘很有用

最近还学习了机器学习方面的知识，tensorflow CNN等逐步探索中
Machine Learning consists of two steps: specify a template and find the best parameters for that template.

https://github.com/nickliqian/cnn_captcha

OCR CNN实现 一个2017研究生

https://medium.com/intuitive-deep-learning/intuitive-deep-learning-part-1a-introduction-to-neural-networks-d7b16ebf6b99

https://medium.com/intuitive-deep-learning/intuitive-deep-learning-part-1b-introduction-to-neural-networks-8565d97ddd2d

So if an image belongs to the first class, the first number of this set will be a 1 and all other numbers in this set will be a 0. This is called a one-hot encoding, and the conversion table now looks like this:
import keras
y_train_one_hot = keras.utils.to_categorical(y_train, 10)
y_test_one_hot = keras.utils.to_categorical(y_test, 10)

At this point, you might want to save your trained model (since you’ve spent so long waiting for it to train). The model will be saved in a file format called HDF5 (with the extension .h5). We save our model with this line of code:

model.save('my_cifar10_model.h5')

You should see the saved model in the directory of your notebook. If you ever want to load your saved model in the future, use this line of code:

from keras.models import load_model
model = load_model('my_cifar10_model.h5')


預測股價的方法還有很多，比如移動平均線、線性回歸、k近鄰、ARIMA和Prophet。讀者可以自行測試這些方法的準確率，並與Keras LSTM的測試結果進行比較。

原文網址：https://kknews.cc/finance/n6962xg.html

https://ithelp.ithome.com.tw/articles/10206312

https://github.com/jimmyleaf/ocr_tensorflow_cnn

https://github.com/xiaofengShi/CHINESE-OCR

https://www.cnblogs.com/skyfsm/archive/2004/01/13/8436820.html

https://sa.sogou.com/sgsearch/sgs_tc_news.php?req=BnMRWbiQj5lytg_WKxersGa52Sn4OdzdzWXAZysYYB4=&user_type=1
基于chineseocr_lite的身份证、火车票、车牌等中文OCR文字识别

文本检测
https://github.com/AstarLight/Lets_OCR/tree/master/detector/ctpn

Paddle OCR
Baidu


v3毫无疑问现在成为了工程界首选的检测算法之一了，结构清晰，实时性好。这是我十分安利的目标检测算法，更值得赞扬的是，yolo_v3给了近乎白痴的复现教程，这种气量在顶层算法研究者中并不常见。你可以很快的用上v3，但你不能很快地懂v3

https://github.com/WenmuZhou/PytorchOCR.git
PytorchOCR旨在打造一套训练，推理，部署一体的OCR引擎库


https://github.com/jimmyleaf/ocr_tensorflow_cnn
最近在研究OCR识别相关的东西，最终目标是能识别身份证上的所有中文汉字+数字，不过本文先设定一个小目标，先识别定长为18的身份证号，当然本文的思路也是可以复用来识别定长的验证码识别的。 本文实现思路主要来源于Xlvector的博客，采用基于CNN实现端到端的OCR，下面引用博文介绍目前基于深度学习的两种OCR识别方法：

https://github.com/xiaofengShi/Image2Katex



https://github.com/eragonruan/text-detection-ctpn

https://github.com/xiaomaxiao/keras_ocr

https://github.com/xiaomaxiao?tab=repositories
很多python有用的东西 pdf 爬虫等

https://github.com/ypwhs/captcha_break

https://blog.csdn.net/qq_32519415/article/details/91044843

https://github.com/gdhy9064/crnn_ctc_simplified_for_digits_keras

https://zhuanlan.zhihu.com/p/35911401
https://github.com/skdjfla/tensorflow-captcha-practice


https://zhuanlan.zhihu.com/p/51866340

http://machinethink.net/blog/

1.手动提取音频文件的特征，因为音频是时域连续的信号，而cnn只能处理空间信息，因此需要将时域信号转换到空间上，常用的音频特征有：mfcc、sfit、mel，以及vggish等，返回一个m*n*c的数组，即该音频文件的特征数组；

2.将该特征数组看成一张图像，送入cnn网络中就可以进行分类了。
https://zhuanlan.zhihu.com/p/63947569


语音AI
https://blog.ailemon.me/2018/11/21/free-open-source-chinese-speech-datasets/

https://juejin.im/post/6844903958033465352

TF PyTorch 基础要打牢

PyTorch
https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html
https://github.com/yunjey/pytorch-tutorial

Keras
https://github.com/erhwenkuo/deep-learning-with-keras-notebooks

TensorFlow
https://github.com/aymericdamien/TensorFlow-Examples


http://vision.stanford.edu/teaching/cs231n/index.html

ML 
https://github.com/nl8590687/Machine-Learning-Tutorial-Chinese

https://zhuanlan.zhihu.com/p/51866340

NuumPY
https://cs231n.github.io/python-numpy-tutorial/

https://github.com/Jack-Cherish/PythonPark

PAPERSWITHCODE

CNN --OCR
CRNN -- 语音 识别 ， 语音合成
CV 机器视觉

https://evilmartians.com/chronicles/learning-how-to-learn-deep-learning




https://colab.research.google.com/notebooks/basic_features_overview.ipynb#scrollTo=Id6tDF1HQSHD


Pytorch 学习
Autograd: Automatic Differentiation

Generally, when you have to deal with image, text, audio or video data, you can use standard python packages that load data into a numpy array. Then you can convert this array into a torch.*Tensor.

For images, packages such as Pillow, OpenCV are useful
For audio, packages such as scipy and librosa
For text, either raw Python or Cython based loading, or NLTK and SpaCy are useful

对n次函数求导函数 只要再前面乘n，n次再降1即可

Specifically for vision, we have created a package called torchvision, that has data loaders for common datasets such as Imagenet, CIFAR10, MNIST, etc. and data transformers for images, viz., torchvision.datasets and torch.utils.data.DataLoader.

This provides a huge convenience and avoids writing boilerplate cod
https://www.shuxuele.com/algebra/index.html


n TensorFlow, packages like Keras, TensorFlow-Slim, and TFLearn provide higher-level abstractions over raw computational graphs that are useful for building neural networks.

In PyTorch, the nn package serves this same purpose. The nn package defines a set of Modules,


forward backward
不断backward 找出微分为0 或者说loss为0的地方的

采用随机梯度下降(Stochastic Gradient Descent, SGD)方法的最简单的更新权重规则如下：

weight = weight - learning_rate * gradient

按照这个规则，代码实现如下所示：



# 简单实现权重的更新例子
learning_rate = 0.01
for f in net.parameters():
    f.data.sub_(f.grad.data * learning_rate)
但是这只是最简单的规则，深度学习有很多的优化算法，不仅仅是 SGD，还有 Nesterov-SGD, Adam, RMSProp 等等，为了采用这些不同的方法，这里采用 torch.optim 库，使用例子如下所示：

https://zhuanlan.zhihu.com/p/60877739

数据科学
最后是数据科学，这个词，听着好像很高大上，其实人家本来就很高大上啦。
对于这个学科我建议你这样理解：
Python 中有一个包叫Pandas，是专门进行数据处理的
同样，还有这样一个包叫Scikit-learn，是进行数据挖掘的
还有像爬虫、可视化Seaborn|matplotlib、线性代数scipy、深度学习keras 等等这样的包，数据科学都涵盖进去了。

https://github.com/double-point/craw_project
数据清洗
https://github.com/double-point/rental_data_analysis

https://github.com/jumper2014/lianjia-beike-spider

https://github.com/jumper2014/Spiders
https://github.com/jumper2014/stock-sky
https://github.com/willowj/python_dataEE

https://juejin.im/entry/6844903961472958471

https://github.com/dawn2004cn/baidu_mp3_to_srt

https://github.com/Python3Spiders/LianJiaSpider

https://github.com/wy9884255/src

https://github.com/yangguichun/ShenzhenHouseInfoCrawler

深圳当前房价数据集 + 深圳10年房价数据历史

anjuke spider
https://juejin.im/post/6844903942468403208

beike
https://www.twblogs.net/a/5e4ff604bd9eee101df8d6c2


量化
房價預測
