# Three Model Compression of NN Surveys’ Summaries & PyTorch Experiment

My literature review consists of three different Models Compression of NN Surveys. For the article tracebility, Mendeley application is used.

In this section, I represent them individually with my brain map. Each diagram was created using the xmind application. The graph of each article was formed while that article was reading. Since they are read at separate times, it does not follow a particular structure. In other words, although graphs have a structure, not every chart has the same structure. However, most of what is meant to be explained in the article refers to the chart by itself. The following table summarizes the surveys:

Table 1: The Summary of Literature Review

| Article Name | Year | Author(s) | Citation |
| --- | --- | --- | --- |
| Literature Review of Deep Network Compression | 2021 | Ali Alqahtani
Xianghua Xie
Mark W. Jones | 1 |
| A Survey of Model Compression and Acceleration for Deep Neural Networks | 2017 | Yu Cheng
Duo Wang
Pan Zhou
Tao Zhang | 484 |
| A Survey on Methods and Theories of Quantized Neural Networks | 2018 | Yunhui Guo | 35 |

## Literature Review of Deep Network Compression

![Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image1.png](Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image1.png)

The article interface is illustrated in Figure 1. The Figure 2 is the graphic that summarizes what the article wants to convey.

![Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image2.png](Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image2.png)

A Survey of Model Compression and Acceleration for Deep Neural Networks

![Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image3.png](Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image3.png)

The figure 3 depicts the article. Then, the graph summarizes it in Figure 4. In Figure 4, there is a red box which is suspicious for me. Because the author states in their table low-rank factorization as easy to implement. Then, in the related section’s Discussion part, they commented exact opposite.

![Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image4.png](Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image4.png)

## A Survey on Methods and Theories of Quantized Neural Networks

![Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image5.png](Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image5.png)

The last survey is specific to quantization which is illustrated in Figure 5. The Figure 6 encompassed the survey.

![Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image6.png](Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image6.png)

Resources

The resources while doing the project are listed in the Jupyter-notebook file. The notebook consists of sections. I added all the links/tabs I opened as a source while completing each section.

# Experiment

I chose Pruning method to compress a pretrained model on CIFAR10 dataset to have less model size and/or faster CPU inference time. For this, I use PyTorch’s pruning. [The link is PyTorch’s Pruning tutorial](https://pytorch.org/tutorials/intermediate/pruning_tutorial.html). I applied L1 pruning for both unstructured and structed way with different amounts/proportion rate. In other words, my two hyperparameters are structuring/not structuring and amount/proportion rate of pruning.

## Hardware Specs & Library Versions

This information is defined in the Jupyter-notebook file: The second and third cells explain library version and hardware specs, respectively.

# Results

## Uncompressed Model

| Model Size | 20M |
| --- | --- |
| CPU Inference Time | 1.4980145456999936 ms |
| Accuracy | 0.9285 |

## Compressed Models

![Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image7.png](Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image7.png)

![Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image8.png](Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image8.png)

The results of each model’s comparisons are illustrated in the following graphs and tables. Figures 7, 8, and 9 are model size, CPU inference time, and accuracy, respectively.

![Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image9.png](Three%20Model%20Compression%20of%20NN%20Surveys%E2%80%99%20Summaries%20&%205fe6f660e51940a9b0a21b4f55e4118f/image9.png)