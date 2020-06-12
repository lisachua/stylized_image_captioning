# Implementing StyleNet: Generating Stylized Image Captions using LSTM
Team: Lisa Chua, Esther Liu

## Introduction
The objective of this project is to implement an image captioning model that has the ability to generate stylized captions (romantic or funny). We will be basing our model on a paper from Microsoft Research Redmond "StyleNet: Generating Attractive Visual Captions with Styles". Our models will be written in Pytorch.

## Data
Our model uses two datasets. The first is the Flickr10k dataset that has an image and factual-caption, this is used for our image captioning task. For our language model, we will use the FlickrStyle 7k dataset published by the authors of the original paper.

## Techniques Overview
<b>LSTM model</b>
We will apply the factored LSTM model from the paper. For image captioning, the commonly used strategies in literature are to adopt a pre- trained CNN model as an encoder to map an image to a fixed dimensional feature vector and then use a LSTM model as the decoder to generate captions based on the image vector. Here, the Factored LSTM model factors the parameters into three matrices to distill the underlying style factors in text data. 

<b>Multi-task training</b>
In the first task, the factored LSTM is trained to generate factual captions given the paired images. In the second task, the factored LSTM is trained as a language model on the romantic or humorous sentences. 


## Evaluation
We will use four metrics that are commonly used in image captioning, including BLEU, METEOR, ROUGE, and CIDEr. For all four metrics, a larger score means better performance. We will compare our model metrics to the ones achieved by in the paper, and other traditional image captioning models like CaptionBot. 


