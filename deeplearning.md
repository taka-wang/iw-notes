# Deep learning

訓練樣本+龐大的計算能力+靈巧的神經網路結構設計

## Resources

- [深度學習 Deep Learning：中文學習資源整理](https://jerrynest.io/deep-learning-resource/)
- [Basic concepts](https://colab.research.google.com/notebooks/mlcc/tensorflow_programming_concepts.ipynb?hl=en#scrollTo=YMG9mHPdzahz)
- [CNN](http://adventuresinmachinelearning.com/convolutional-neural-networks-tutorial-tensorflow/)
- [RNN](http://adventuresinmachinelearning.com/recurrent-neural-networks-lstm-tutorial-tensorflow/)
- [Transfer learning](http://cs231n.github.io/transfer-learning/)
- [Keras resources: Is Keras better than Tensorflow for deep learning](http://qr.ae/TU1Crg)
- [Intro pandas](https://colab.research.google.com/notebooks/mlcc/intro_to_pandas.ipynb?hl=en#scrollTo=hMqWDc_m6rUC)
- [A Gentle Introduction to Transfer Learning for Deep Learning](https://machinelearningmastery.com/transfer-learning-for-deep-learning/)
- [淺談Alpha Go所涉及的深度學習技術](https://www.bnext.com.tw/article/38923/BN-2016-03-14-120814-178)
- [Machine Learning Crash Course](https://developers.google.com/machine-learning/crash-course/)
- [YOLO Object Detection](https://www.youtube.com/watch?v=4eIBisqx9_g)
- [第5.1講: 卷積神經網絡介紹(Convolutional Neural Network)](https://goo.gl/MDJbKt)
- [Where-can-I-start-learning-how-to-use-TensorFlow](https://www.quora.com/Where-can-I-start-learning-how-to-use-TensorFlow)
- [TensorFlow and deep learning, without a PhD](https://codelabs.developers.google.com/codelabs/cloud-tensorflow-mnist/index.html?index=..%2F..%2Findex#0)


## Applications

- [Real-Time Ingesting and Transforming Sensor Data and Social Data with NiFi and TensorFlow](https://www.slideshare.net/Hadoop_Summit/realtime-ingesting-and-transforming-sensor-data-and-social-data-with-nifi-and-tensorflow)
- [Real Time Object Detection with TensorFlow Detection Model](https://towardsdatascience.com/real-time-object-detection-with-tensorflow-detection-model-e7fd20421d5d)
- [Deep Learning Projects by Udacity Students](https://medium.com/self-driving-cars/deep-learning-projects-by-udacity-students-cec150d4321d)
- [USING IOT AND MACHINE LEARNING FOR INDUSTRIAL PREDICTIVE MAINTENANCE](https://www.losant.com/blog/using-iot-and-machine-learning-for-industrial-predictive-maintenance)
- [How a Japanese cucumber farmer is using deep learning and TensorFlow](https://cloud.google.com/blog/big-data/2016/08/how-a-japanese-cucumber-farmer-is-using-deep-learning-and-tensorflow)
- [Machine Learning Techniques for Predictive Maintenance](https://www.infoq.com/articles/machine-learning-techniques-predictive-maintenance)
- [Machine learning for predictive maintenance: where to start?](https://medium.com/bigdatarepublic/machine-learning-for-predictive-maintenance-where-to-start-5f3b7586acfb)
- [[Tutorial] building machine learning models for predictive maintenance applications - Yan Zhang](https://www.slideshare.net/papisdotio/tutorial-building-machine-learning-models-for-predictive-maintenance-applications-yan-zhang)
- [Continuous online video classification with TensorFlow, Inception and a Raspberry Pi](https://blog.coast.ai/continuous-online-video-classification-with-tensorflow-inception-and-a-raspberry-pi-785c8b1e13e1)
- [Implement Object Recognition on Livestream](https://dzone.com/articles/implement-object-recognition-on-live-stream)
- [How to Build a Real-time Hand-Detector using Neural Networks (SSD) on Tensorflow](https://towardsdatascience.com/how-to-build-a-real-time-hand-detector-using-neural-networks-ssd-on-tensorflow-d6bac0e4b2ce)
- [Building a Real-Time Object Recognition App with Tensorflow and OpenCV](https://towardsdatascience.com/building-a-real-time-object-recognition-app-with-tensorflow-and-opencv-b7a2b4ebdc32)
- [Detect suspicious activity](https://dzone.com/articles/video-analysis-to-detect-suspicious-activity-based)
- [A Deep Hybrid Learning Model to Detect Unsafe Behavior: Integrating Convolution Neural Networks and Long Short-Term Memory](https://www.researchgate.net/publication/320820471_A_Deep_Hybrid_Learning_Model_to_Detect_Unsafe_Behavior_Integrating_Convolution_Neural_Networks_and_Long_Short-Term_Memory)
- [Deep learning for sensor-based human activity recognition](https://becominghuman.ai/deep-learning-for-sensor-based-human-activity-recognition-970ff47c6b6b)
- [使用 TensorFlow 來做簡單的手寫數字辨識](https://blog.techbridge.cc/2018/01/27/tensorflow-mnist/)
- [Creating a Modern OCR Pipeline Using Computer Vision and Deep Learning](https://blogs.dropbox.com/tech/2017/04/creating-a-modern-ocr-pipeline-using-computer-vision-and-deep-learning/)
- [Deep Pose Estimation implemented using Tensorflow with Custom Architecture for fast inference.](https://github.com/ildoonet/tf-pose-estimation)
- [LSTM-Human-Activity-Recognition](https://github.com/guillaume-chevalier/LSTM-Human-Activity-Recognition)
- [Human Fall Detection in Indoor Environments Using Channel State](http://cs229.stanford.edu/proj2016/report/NaruiDayalDeligiannis-HumanFallDetectionUsingWiFi-report.pdf)
- [Multivariate Time Series Forecasting with LSTMs in Keras](https://machinelearningmastery.com/multivariate-time-series-forecasting-lstms-keras/)
- [Pre-Collision Assist with Pedestrian Detection - TensorFlow](https://www.hackster.io/asadzia/pre-collision-assist-with-pedestrian-detection-tensorflow-db91cb)
- [Music applications](http://www.asimovinstitute.org/analyzing-deep-learning-tools-music/)

---


## Tensorflow

### Terms
- tensor: arrays of arbitrary dimensionality
- operations: create, destroy and manipulate tensors
- graph: computational graph or dataflow graph
  - node: operation
  - edge: tensor

### Two steps process
TensorFlow programming is essentially a two-step process:

- Assemble constants, variables, and operations into a graph.
- Evaluate those constants, variables and operations within a session.
- **lazy execution model**

### Serving

- [How to deploy an object detection model with tensorflow serving](https://medium.freecodecamp.org/how-to-deploy-an-object-detection-model-with-tensorflow-serving-d6436e65d1d9)
- [How Zendesk Serves TensorFlow Models in Production](https://medium.com/zendesk-engineering/how-zendesk-serves-tensorflow-models-in-production-751ee22f0f4b)
- [How to Deploy a Tensorflow Model to Production - YouTube](https://www.youtube.com/watch?v=T_afaArR0E8)
- [GPUs & Kubernetes for Deep Learning — Part 3/3: Automating Tensorflow deployment](https://medium.com/intuitionmachine/gpus-kubernetes-for-deep-learning-part-3-3-automating-tensorflow-deployment-5dc4d5472e91)
- [2018 Fun with Kubernetes & Tensorflow Serving](https://itnext.io/fun-with-kubernetes-tensorflow-serving-4fef8d7502b9)

### Examples

- Hello world

```python
import tensorflow as tf
hello = tf.constant("hello")
sess = tf.Session()
print(sess.run(hello))
```

- Constant

`x = tf.constant(5.2)`

- Variable

```python
y = tf.Variable([5])
y = y.assign([3]) # assign a new value
```

- Addition

```python
import tensorflow as tf

# Create a graph.
g = tf.Graph()

# Establish the graph as the "default" graph.
with g.as_default():
  # Assemble a graph consisting of the following three operations:
  #   * Two tf.constant operations to create the operands.
  #   * One tf.add operation to add the two operands.
  x = tf.constant(8, name="x_const")
  y = tf.constant(5, name="y_const")
  my_sum = tf.add(x, y, name="x_y_sum")


  # Now create a session.
  # The session will run the default graph.
  with tf.Session() as sess:
    print my_sum.eval()
```

