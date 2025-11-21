# Object Detection Benchmark on TCC807x

The following table shows benchmark results for various Object Detection network models running on the **TCC807x** NPU.
You can compare the performance of each model.

Click on the model name to download a tar file containing the model binary for TCC807x.

---

<!-- ![OD Model Performance](../../docs/image/od_performance.png) -->

### 📊 Table Overview

| Column                    | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **Model**                | Name of the neural network model      |
| **Framework**            | Deep learning framework used (e.g., PyTorch, TFLite, ONNX)                  |
| **Dataset**              | Dataset used to benchmark model performance                                                          |
| **Input Size (WxHxC)**   | Input Size (Width × Height × Channels) of the input image required by the model                            |
| **Inference Time (ms)**  | Inference time measured on the TCC807x EVB using zero-padded input images                               |
| **mAP**             | Mean Average Precision (mAP) is evaluated on the **COCO2017 validation dataset** (5,000 images)                    |
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
            <td align="center" class="variant"><a href="SSDlite/ssdlite_mobilenet_v1">mb1</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">300x300x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">16.58</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.344</td> <!-- Evaluation Result: FP32 -->
            <td align="right">0.341</td> <!-- Evaluation Result: INT8 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">40.264</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">246.224</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">57.569</td> <!-- Compiled NN Information: Network (.so) (MB) -->
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
            <td align="right">29.528</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">1.744</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">470.603</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/ultralytics/yolov3">Github<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov3/yolov3_tiny/">tiny</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">2.50</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.338</td> <!-- Evaluation Result: FP32 IoU=0.50 -->
            <td align="right">0.319</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">17.624</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.256</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">63.818</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/ultralytics/yolov3">Github<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" rowspan="1" class="model"><a href="YOLO/yolov4/README.md">YOLOv4</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolov4/yolov4">-</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">608x608x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">41.59</td>
            <td align="right">0.476</td>
            <td align="right">0.252</td>
            <td align="center">INT8</td>
            <td align="right">2.363</td>
            <td align="right">0.032</td>
            <td align="right">63.506</td>
            <td align="center"><a href="https://github.com/AlexeyAB/darknet">Github<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" rowspan="4" class="model"><a href="YOLO/yolov6/README.md">YOLOv6</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolov6/yolov6n/">n</a></td> <!-- Models: Variant -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">39.39</td>
            <td align="right">0.389</td>
            <td align="right">0.342</td>
            <td align="center">INT8</td>
            <td align="right">16.348</td>
            <td align="right">0.14</td>
            <td align="right">5.033</td>
            <td align="center" rowspan="4"><a href="https://github.com/meituan/YOLOv6">GitHub<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov6/yolov6s/">s</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">60.52</td>
            <td align="right">0.446</td>
            <td align="right">0.407</td>
            <td align="center">INT8</td>
            <td align="right">16.302</td>
            <td align="right">0.14</td>
            <td align="right">17.468</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov6/yolov6m/">m</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">83.51</td>
            <td align="right">0.471</td>
            <td align="right">0.437</td>
            <td align="center">INT8</td>
            <td align="right">16.56</td>
            <td align="right">0.194</td>
            <td align="right">32.138</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov6/yolov6l/">l</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">1414.80</td>
            <td align="right">0.488</td>
            <td align="right">0.461</td>
            <td align="center">INT8</td>
            <td align="right">208.664</td>
            <td align="right">2.066</td>
            <td align="right">62.854</td>
        </tr>
        <tr>
            <td align="center" rowspan="5" class="model"><a href="YOLO/yolov8/README.md">YOLOv8</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolov8/yolov8n/">n</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">14.57</td>
            <td align="right">0.479</td>
            <td align="right">0.382</td>
            <td align="center">INT8</td>
            <td align="right">1.722</td>
            <td align="right">0.032</td>
            <td align="right">3.577</td>
            <td align="center" rowspan="5"><a href="https://github.com/ultralytics/ultralytics">GitHub<a></td> <!-- References: Link -->
        </tr>
    </tbody>
</table>

- - -

### Footnote
* All models in this repository are distributed exclusively in TensorFlow Lite® format.
* TFLite® and ONNX™ are not provided.
