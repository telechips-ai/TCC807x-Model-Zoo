
# **TCC807x (Dolphin 5) Model Zoo**
<a href="https://www.telechips.com/view/technology/prod03" target="_blank">
    <img src="./_docs/image/dolphin_5.png" alt="Dolphin 5 Image">
</a>

This repository provides a collection of neural network models optimized for Telechips Cockpit (TCC807x).

The models are ready to run on evaluation boards and include benchmark results that show how the TCC807x performs.

---

## **1. Chip Description**
The TCC807x features an integrated Neural Processing Unit (NPU).
With support for up to 8 TOPS, the TCC807x redefines in-car innovation with scalable, integrated solutions tailored for both infotainment and advanced driver assistance systems (ADAS).

### TCC807x (D5)
- **Performance:** 8 TOPS
- **Target Applications:**
  - Advanced driver assistance systems (ADAS)
  - Vision-based applications (multi-camera processing)
  - Driver Monitoring System (DMS)
  - Deep learning inference

With an integrated NPU, the TCC807x delivers real-time neural network inference with high efficiency and scalable performance for automotive applications.

---

## **2. Overview of Model Zoo**
The following table summarizes the image classification and object detection models supported on TCC807x.
Each model name links to its dedicated page with performance metrics and deployment instructions.

**Note:** The models covered in this document are based on original network architectures or have been minimally modified for compatibility with TCC807x execution. The results shown are not guaranteed for production use, and you are responsible for any further optimization.

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
            <td align="right">1.30</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.723</td> <!-- Accuracy -->
        </tr>
        <tr>
            <td align="center" colspan="2">MobileNet-v2-1.4</td> <!-- Model -->
            <td align="center">224x224x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">1.14</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.699</td> <!-- Accuracy -->
        </tr>
        <tr>
            <td align="center" colspan="2">ResNet50-v2</td> <!-- Model -->
            <td align="center">224x224x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">5.54</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.712</td> <!-- Accuracy -->
        </tr>
        <tr>
            <td align="center" colspan="2">LeNet5</td> <!-- Model -->
            <td align="center">224x224x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">0.19</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.970</td> <!-- Accuracy -->
        </tr>
    </tbody>
<table>

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
            <td align="right">16.58</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.341</td>
        </tr>
        <tr>
            <td align="center" rowspan="2" class="model">YOLOv3</td> <!-- Model -->
            <td align="center" class="variant">-</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">47.32</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.426</td>
        </tr>
        <tr>
            <td align="center" class="variant">tiny</td> <!-- Model -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">5.25</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.215</td>
        </tr>
        <tr>
            <td align="center" colspan="2">YOLOv4</td> <!-- Model -->
            <td align="center">608x608x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">47.51</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.446</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" rowspan="4" class="model">YOLOv6</td> <!-- Models -->
            <td align="center" class="variant">n</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">11.47</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.328</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">s</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">14.52</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.352</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">m</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">20.79</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.424</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">l</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">29.90</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.427</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" rowspan="2" class="model">YOLOv7</td> <!-- Models -->
            <td align="center" class="variant">-</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">41.39</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.459</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">tiny</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">27.62</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.381</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" rowspan="5" class="model">YOLOv8</td> <!-- Models -->
            <td align="center" class="variant">n</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">18.44</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.347</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">s</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">21.73</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.391</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">m</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">28.00</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.435</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">l</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">36.92</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.450</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">x</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">46.21</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.456</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" rowspan="1" class="model">YOLOv9</td> <!-- Models -->
            <td align="center" class="variant">s</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">32.44</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.328</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" rowspan="6" class="model">YOLOX</td> <!-- Models -->
            <td align="center" class="variant">nano</td> <!-- Models: Variant -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">14.28</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.059</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">tiny</td> <!-- Models: Variant -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">14.87</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.305</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">s</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">33.83</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.281</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">m</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">40.83</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.257</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">l</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">51.30</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.409</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
        <tr>
            <td align="center" class="variant">x</td> <!-- Models: Variant -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">65.62</td> <!-- Inference Time (msec): EVB -->
            <td align="right">0.502</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
        </tr>
    </tbody>
<table>

---

## **3. Getting Started**
Follow these steps to run a model provided by Telechips Model Zoo on the TCC807x Evaluation Board (EVB).

### 1. Clone the repository:
<pre> <code>
git clone git@github.com:telechips-ai/TCC807x-Model-Zoo.git
</code> </pre>

### 2. Copy the desired model to the EVB:
Copy the entire model folder (ssdlite_mobilenet_v1) to the TCC807x EVB.
Each folder contains the necessary output files (.so, .json, and .param).
<pre> <code>
scp -r [network_output_folder] root@192.168.0.100:/path/to/target/
</code> </pre>
Replace [network_output_folder] with the actual folder (e.g., ssdlite_mobilenet_v1/).

### ***Example: TCC807x - ssdlite_mobilenet_v1 Folder Structure***
<pre> <code>
ssdlite_mobilenet_v1/
├── mod.so        # Compiled model
├── mod.json      # Model graph
└── mod.param     # Binary file of Quantized weight and bias
</code> </pre>
Then run:
<pre> <code>
scp -r ssdlite_mobilenet_v1/ root@192.168.0.100:/home/root/
</code> </pre>

### 3. Run the model using rtvm:
<pre> <code>
rtvm --model=[network_output_folder_path] --device=cpu --dump-meta --profile --run-count=10
</code> </pre>

---

## 4. **Requirement**

* ethos-n-driver-stack: 25.03
* TVM: 0.18.0
    * Python: 3.10
    * Clang/LLVM: clang+llvm-11.0.0-x86_64-linux-gnu-ubuntu-20.04
    * GCC for Arm: gcc-arm-9.2-2019.12-x86_64-aarch64-none-linux-gnu

---
## 5. **License**
* Model: For each model’s license, please refer to the License block.

* Dataset

| Dataset        | SPDX Identifier  | Full Name                              | Link                                                                     |
| -------------- | ---------------- | -------------------------------------- | ------------------------------------------------------------------------ |
| **COCO2017**   | CC-BY-4.0        | Creative Commons Attribution 4.0 International | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)  |
| **ILSVRC2012** | ImageNet Terms of Use | ImageNet Terms of Use                     | [ImageNet](https://www.image-net.org/)                     |
