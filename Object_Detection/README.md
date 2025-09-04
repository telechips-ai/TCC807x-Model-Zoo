# Object Detection Benchmark on TCC807x

The following table shows benchmark results for various Object Detection network models running on the **TCC807x** NPU.  
You can compare the performance of each model.

Click on the model name to download a tar file containing the model binary for TCC807x.

---

<!-- ![OD Model Performance](../../docs/image/od_performance.png) -->

### 📊 Table Overview

| Column                    | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **Model**                | Name of the object detection model      |
| **Framework**            | Deep learning framework used (e.g., PyTorch, TFLite, ONNX)                  |
| **Dataset**              | Dataset used to benchmark model performance                                                          |
| **Input Size (WxHxC)**   | Input Size (Width × Height × Channels) of the input image required by the model                            |
| **Inference Time (ms)**  | Inference time measured on the TCC807x EVB using zero-padded input images.                               |
| **mAP**             | Mean Average Precision (mAP), evaluated on **COCO2017 validation dataset** (5,000 images)                    |
| **Quantization Bit**     | Bit-depth used for quantization (e.g., INT8)                                |
| **Compiled Model Files**   | Sizes of the compiled model components: .json, .params, and .so for execution on TCC807x                     |
| **References**           | Link to the original GitHub repository of the model                         |

---
<table border="1" cellspacing="0" cellpadding="5">
    <thead>
        <tr>
            <th align="center" rowspan="2" colspan="2">Model</th>
            <th rowspan="2">Framework</th>
            <th rowspan="2">Dataset</th>
            <th rowspan="2">Input Size (WxHxC)</th>
            <th rowspan="2">Inference Time (ms)</th>
            <th colspan="2">mAP@50</th>
            <th rowspan="2">Quantization Bit</th>
            <th colspan="3">Compiled Model Files</th>
            <th rowspan="2">References</th>
        </tr>
        <tr>
            <th>FP32</th>
            <th>INT8</th>
            <th>.json (KB)</th>
            <th>.params (KB)</th>
            <th>.so (MB)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center" rowspan="1" class="model"><a href="SSDlite/README.md">SSDlite</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="SSDlite/ssdlite_mobilenet_v1/">mb1</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">300x300x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">16.58</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.344</td> <!-- Evaluation Result: FP32 -->
            <td align="right">0.341</td> <!-- Evaluation Result: INT8 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">40.26</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">246.22</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">57</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/tensorflow/models/blob/f007603b50b4db38907594a156994a4e983d2d31/research/object_detection/g3doc/tf1_detection_zoo.md">Github<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" rowspan="2" class="model"><a href="YOLO/yolov3/README.md">YOLOv3</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolov3/yolov3/"> - </a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">15.21</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.588</td> <!-- Evaluation Result: FP32 IoU=0.50 -->
            <td align="right">0.560</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">29.52</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">1.74</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">470</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/ultralytics/yolov3">Github<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov3/yolov3-tiny/">tiny</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">2.50</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.338</td> <!-- Evaluation Result: FP32 IoU=0.50 -->
            <td align="right">0.319</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">17.62</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.25</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">63</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/ultralytics/yolov3">Github<a></td> <!-- References: Link -->
        </tr>
    </tbody>
</table>

- - -

### Footnote                
* All models in this repository are distributed exclusively in TensorFlow Lite® format.  
* PyTorch® and ONNX™ are not provided.