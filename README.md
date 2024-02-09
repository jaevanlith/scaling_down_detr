# Scaling down with DETR

This repository contains a blog post in the form of a Jupyter notebook. Please consult the instructions to either run remotely or locally.

## Authors
Jeroen Hofland (j.l.hofland@student.tudelft.nl)
Jochem van Lith (j.a.e.vanlith@student.tudelft.nl)

## Introduction
Object detection is a crucial task in computer vision that plays an important role in various applications, ranging from automating tasks and enhancing image understanding to improving security surveillance systems. In recent years, significant advancements have been made in this field, with the emergence of new methods that use Transformers [1].

One such an approach is the DEtection TRansformer (DETR), which revolutionized object detection with its end-to-end architecture and self-attention mechanisms based on transformers [2]. This allows the method to tackle object detection in a more comprehensive way by both looking at local and global spatial features.

By doing so the method surpassed traditional approaches like YOLO [3] and Faster R-CNN [4] in many aspects. However, one area where DETR struggles is detecting small objects within images. Recent advancements aimed at addressing this limitation are DEtection Split TRansformer (DESTR) and SOF-DETR [5,6]. While these methods yield a slight increase of accuracy on small objects, it is still around half of that of medium and large objects. Therefore, it remains crucial to understand when and why DETR encounters difficulties detecting small objects.

The size of an object is determined by its number of pixels. In other words, small objects are inherently represented by less pixels making detection more challenging. Now if this is what causes DETR's problems with small objects, then it will also be highly sensitive to lower resolution images. We aim to investigate this by asking the following experimental question:

How does the Average Precision per object size change for lower resolution images?

In this blog we will explain DETR, introduce the performed experiments, present the results, and end with a conclusion.

## Instructions
Python version >= 3.10.8

#### Run remotely (recommended)
Run remotely by following the instructions here: [https://colab.research.google.com/drive/1HYg_QNXmVyKal2i0oIqehxpkD7IccpbW?usp=sharing](https://colab.research.google.com/drive/1F__L7UjpJuObXKf-jLLLfJLjq3NUS6m9#scrollTo=xNkBHx5MFaH5)

#### Local installation
Clone the repository to your device and run the notebook in your favourite IDE.
