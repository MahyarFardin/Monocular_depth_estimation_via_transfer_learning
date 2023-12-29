# Monocular_depth_estimation_via_transfer_learning
This repository contains the regeneration of an impactful paper called by the repositories name. The code is implemented in PyTorch despite the paper reporting its achievements in TensorFlow. Here is the [link to the paper](https://arxiv.org/pdf/1812.11941v2.pdf)

# Title and Description

The paper "High Quality Monocular Depth Estimation via Transfer Learning" focuses on the task of depth estimation from images, which is a fundamental task in various applications, including scene understanding and reconstruction. The authors propose a convolutional neural network (CNN) that computes a high-resolution depth map given a single RGB image using transfer learning. Key points from the paper include:

- **Encoder-decoder architecture:** The network follows a standard encoder-decoder architecture, leveraging features extracted using high-performing pre-trained networks to initialize the encoder, along with augmentation and training strategies for more accurate results.
- **Transfer learning:** The authors use transfer learning to improve the quality and resolution of depth estimation. This approach allows the network to learn from large-scale datasets, enabling it to generate more accurate and detailed depth maps.
- **Comparison with state-of-the-art:** The proposed method outperforms state-of-the-art on two datasets and produces qualitatively better results that capture object boundaries more faithfully.
- **Benchmarks and datasets:** The paper is part of the Monocular Depth Estimation task on Papers with Code, which includes 303 papers with code, 18 benchmarks, and 25 datasets.
- The most popular benchmarks are the KITTI and NYUv2 datasets, and models are typically evaluated using RMSE or absolute relative error which I used NYU dataset.

In summary, the paper presents a novel approach to monocular depth estimation using transfer learning, demonstrating improved quality and resolution compared to existing methods. The proposed approach has the potential to enhance various applications that rely on accurate depth estimation, such as scene understanding, autonomous driving, and augmented reality.

# Acknowledge
Though the paper was implemented in TensorFlow I confronted many issues but I almost overcame all of them, except a significant major issue; **according to the paper the last layer before the decoder should be a layer with a depth of 1664, but according to our default model in PyTorch, the mentioned layer has 1632 layers**. This was a major issue that I tried to resolve by adding another convolutional layer to project it to my desired dimensionality.

