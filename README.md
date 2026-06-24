
# **TCC807x (Dolphin 5) Model Zoo**
<a href="https://www.telechips.com/view/technology/prod03" target="_blank">
    <img src="./_docs/image/dolphin_5.png" alt="Dolphin 5 Image">
</a>

This repository provides a collection of neural network models optimized for Telechips Cockpit (TCC807x).

The models are ready to run on the TCC807x Evaluation Board (EVB) and include benchmark results that show how the TCC807x performs.

---

## **1. Chip Description**
The TCC807x features an integrated Neural Processing Unit (NPU).
With support for up to 8 TOPS, the TCC807x redefines in-car innovation with scalable solutions tailored for both infotainment and advanced driver assistance systems (ADAS).

### TCC807x (D5)
- **Performance:** 8 TOPS
- **Target Applications:**
  - Advanced driver assistance systems (ADAS)
  - Vision-based applications (multi-camera processing)
  - Driver Monitoring System (DMS)
  - Deep learning inference

With its NPU, the TCC807x delivers real-time neural network inference with high efficiency and scalable performance for automotive applications.

---

## **2. Overview of Model Zoo**
The following table summarizes the image classification and object detection models supported on the TCC807x.
Each model name links to its dedicated page with performance metrics and deployment instructions.

**Note:** The models covered in this document are based on original network architectures or have been minimally modified for compatibility with the TCC807x. The results shown are not guaranteed for production use, and you are responsible for any further optimization.

### [Classification](Classification/README.md)

<table border="1" cellspacing="0" cellpadding="5" style="width:100%; table-layout:fixed;">
    <thead>
        <tr>
            <th rowspan="2" colspan="2">Model</th>
            <th rowspan="2">Input Size (WxHxC)</th>
            <th rowspan="2">Inference Time (ms)</th>
            <th rowspan="2">Accuracy</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center" colspan="2">EfficientNet-Lite0</td> <!-- Model -->
            <td align="center">224x224x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">1.75</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.749</td> <!-- Accuracy -->
        </tr>
        <tr>
            <td align="center" colspan="2">MobileNet-v2-1.0</td> <!-- Model -->
            <td align="center">224x224x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">1.52</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.712</td> <!-- Accuracy -->
        </tr>
        <tr>
            <td align="center" colspan="2">ResNet50-v2</td> <!-- Model -->
            <td align="center">224x224x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">5.02</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.704</td> <!-- Accuracy -->
        </tr>
        <tr>
            <td align="center" colspan="2">LeNet5</td> <!-- Model -->
            <td align="center">32x32x1</td> <!-- Input Size (WxHxC) -->
            <td align="right">0.25</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.985</td> <!-- Accuracy -->
        </tr>
    </tbody>
</table>

### [Object Detection](Object_Detection/README.md)

<table border="1" cellspacing="0" cellpadding="5" style="width:100%; table-layout:fixed;">
    <thead>
        <tr>
            <th rowspan="2" colspan="2">Model</th>
            <th rowspan="2">Input Size (WxHxC)</th>
            <th rowspan="2">Inference Time (ms)</th>
            <th rowspan="2">mAP@50</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center" colspan="2">SSDlite-MobileNet-v1</td> <!-- Model -->
            <td align="center">300x300x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">4.24</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.386</td>
        </tr>
        <tr>
            <td align="center" rowspan="2" class="model">YOLOv3</td> <!-- Model -->
            <td align="center" class="variant">tiny</td> <!-- Model -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">8.11</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.305</td>
        </tr>
        <tr>
            <td align="center" class="variant">-</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">96.94</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.558</td>
        </tr>
        <tr>
            <td align="center" colspan="2">YOLOv4</td> <!-- Model -->
            <td align="center">608x608x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">52.17</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.592</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" rowspan="5" class="model">YOLOv5</td> <!-- Models -->
            <td align="center" class="variant">n</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">30.99</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.251</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">s</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">39.28</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.506</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">m</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">56.70</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.572</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">l</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">81.37</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.607</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">x</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">115.67</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.620</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" rowspan="4" class="model">YOLOv6</td> <!-- Models -->
            <td align="center" class="variant">n</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">12.40</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.346</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">s</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">17.36</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.409</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">m</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">25.53</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.535</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">l</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">73.49</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.586</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" rowspan="2" class="model">YOLOv7</td> <!-- Models -->
            <td align="center" class="variant">tiny</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">27.24</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.489</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">-</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">83.11</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.616</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" rowspan="5" class="model">YOLOv8</td> <!-- Models -->
            <td align="center" class="variant">n</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">23.93</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.440</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">s</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">34.01</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.541</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">m</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">52.57</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.584</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">l</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">78.75</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.601</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">x</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">102.03</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.610</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" rowspan="1" class="model">YOLOv9</td> <!-- Models -->
            <td align="center" class="variant">s</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">40.84</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.345</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" rowspan="6" class="model">YOLOX</td> <!-- Models -->
            <td align="center" class="variant">nano</td> <!-- Models: Variant -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">11.29</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.038</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">tiny</td> <!-- Models: Variant -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">13.11</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.362</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">s</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">30.97</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.447</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">m</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">52.01</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.507</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">l</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">82.25</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.527</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">x</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">123.34</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.556</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
    </tbody>
</table>

---

## **3. Getting Started**
Follow these steps to run a model provided by Telechips Model Zoo on the TCC807x Evaluation Board.

### 1. Clone the repository:
<pre> <code>
git clone git@github.com:telechips-ai/TCC807x-Model-Zoo.git
</code> </pre>

### 2. Copy the desired model to the EVB:
Copy the model folder (e.g., ssdlite_mobilenet_v1) to the TCC807x EVB.
Each folder contains a `.tar` archive (e.g., ssd_mobilenet_v1_int8.tar) of the output files (.so, .json, and .params).
<pre> <code>
scp -r [network_output_folder] root@192.168.0.100:/path/to/target/
</code> </pre>
Replace [network_output_folder] with the actual folder (e.g., ssdlite_mobilenet_v1/).
Then run:
<pre> <code>
scp -r ssdlite_mobilenet_v1/ root@192.168.0.100:/home/root/
</code> </pre>

### 3. Extract the model archive:
Extract the `.tar` archive to obtain the output files (.so, .json, and .params) required by rtvm.
<pre> <code>
tar xf [model_name]_int8.tar
</code> </pre>

### ***Example: TCC807x - ssdlite_mobilenet_v1 Folder Structure***
<pre> <code>
ssdlite_mobilenet_v1/
├── mod.so        # Compiled model
├── mod.json      # Model graph
└── mod.params    # Quantized weights and biases (binary)
</code> </pre>

### 4. Run the model using rtvm:
<pre> <code>
rtvm --model=[network_output_folder_path] --device=cpu --dump-meta --profile --run-count=10
</code> </pre>

---

## **4. Requirements**

* ethos-n-driver-stack: 25.03 (modified for TCC807x)
* TVM: 0.18.0 (modified for TCC807x)
    * Python: 3.10
    * Clang/LLVM: clang+llvm-11.0.0-x86_64-linux-gnu-ubuntu-20.04
    * GCC for Arm: gcc-arm-9.2-2019.12-x86_64-aarch64-none-linux-gnu

---
## **5. License**
* Model: For each model's license, refer to the License section.

* Dataset

| Dataset        | SPDX Identifier  | Full Name                              | Link                                                                     |
| -------------- | ---------------- | -------------------------------------- | ------------------------------------------------------------------------ |
| **COCO2017**   | CC-BY-4.0        | Creative Commons Attribution 4.0 International | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)  |
| **ILSVRC2012** | ImageNet Terms of Use | ImageNet Terms of Use                     | [ImageNet](https://www.image-net.org/)                     |
| **MNIST**      | CC-BY-SA-3.0     | Modified National Institute of Standards and Technology database | [MNIST](http://yann.lecun.com/exdb/mnist/)        |
