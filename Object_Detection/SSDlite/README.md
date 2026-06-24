# SSDlite Benchmark on TCC807x

The following table shows benchmark results for the SSDlite-MobileNet-v1 model running on the **TCC807x** NPU.  
SSDlite is a lightweight and efficient object detection model designed for mobile and embedded devices, offering a good trade-off between speed and accuracy.
SSDlite is a variant of the original SSD model with depthwise separable convolutions for reduced computation.

Click on the model name to download a tar file containing the model binary for TCC807x.  

---

### 📊 Table Overview

| Column                    | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **Model**                | Name of the neural network model    |
| **Framework**            | Deep learning framework used (e.g., PyTorch, TFLite, ONNX)                  |
| **Dataset**              | Dataset used to benchmark model performance                                                         |
| **Input Size (WxHxC)**   | Input Size (Width × Height × Channels) of the input image required by the model                           |
| **Inference Time (ms)**  | Inference time measured on the TCC807x EVB using zero-padded input images                               |
| **mAP**             | Mean Average Precision evaluated on the **COCO2017 validation** set (5,000 images) — **FP32** measured on PC, **INT8** on the TCC807x EVB.                    |
| **Quantization Bit**     | Bit-depth used for quantization (e.g., INT8)                                |
| **Compiled Model Files**   | Sizes of the compiled model components: .json, .params, and .so for execution on TCC807x                     |
| **References**           | Link and license** information for the original repository of the model                         |

---
<table border="1" cellspacing="0" cellpadding="5">
    <thead>
        <tr>
            <th align="center" rowspan="2" colspan="2">Model</th>
            <th align="center" rowspan="2">Framework</th>
            <th align="center" rowspan="2">Dataset</th>
            <th align="center" rowspan="2">Input Size (WxHxC)</th>
            <th align="center" rowspan="2">Inference Time (ms)</th>
            <th align="center" colspan="2">mAP@50:95</th>
            <th align="center" colspan="2">mAP@50</th>
            <th align="center" rowspan="2">Quantization Bit</th>
            <th align="center" colspan="3">Compiled Model Files</th>
            <th align="center" colspan="2">References</th>
        </tr>
        <tr>
            <th>FP32</th>
            <th>INT8</th>
            <th>FP32</th>
            <th>INT8</th>
            <th>.json (KB)</th>
            <th>.params (KB)</th>
            <th>.so (MB)</th>
            <th>Link</th>
            <th>License</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center" rowspan="1" class="model">SSDlite</td> <!-- Model -->
            <td align="center" rowspan="1" class="variant"><a href="ssdlite_mobilenet_v1/">mb1</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">300x300x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">4.24</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.236</td> <!-- Evaluation Result: FP32 IoU=0.50:0.95 -->
            <td align="right">0.234</td> <!-- Evaluation Result: INT8 IoU=0.50:0.95 -->
            <td align="right">0.389</td> <!-- Evaluation Result: FP32 IoU=0.50 -->
            <td align="right">0.386</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">2.059</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.031</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">6.724</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/tensorflow/models/blob/f007603b50b4db38907594a156994a4e983d2d31/research/object_detection/g3doc/tf1_detection_zoo.md">GitHub</a></td> <!-- References: Link -->
            <td align="center">Apache-2.0</td>
        </tr>
    </tbody>
</table>

- - -

## 📤 Output Format

- The raw output of an SSDlite model consists of anchor-relative box encodings and per-class logits (including a background class).
- These raw outputs require the following post-processing:
  - Decoding the box encodings into bounding boxes using the anchor boxes
  - Applying sigmoid activation to normalize outputs
  - Filtering boxes based on confidence thresholds
  - Applying Non-Maximum Suppression (NMS) to remove overlapping boxes

- The final post-processed output includes a list of detected objects, each containing:
  - Class label
  - Confidence score
  - Bounding box coordinates (x_min, y_min, x_max, and y_max)

- - -

### Footnote                
* All models in this repository are distributed exclusively as a compiled `.tar` archive for the TCC807x.  
* The source models (PyTorch®, ONNX™, and TensorFlow Lite®) are not provided.
* License\**:
  - Telechips Inc. is not responsible for any issues, damages, or losses resulting from the use of code downloaded from GitHub repositories provided by Telechips.
  - The performance results of neural networks (such as mAP or inference time) are not subject to license terms and may be used freely.
  - Any output generated by software execution may or may not be subject to license terms, depending on the contract and intended use of the output.