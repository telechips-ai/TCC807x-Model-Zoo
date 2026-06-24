# Object Detection Benchmark on TCC807x

The following table shows benchmark results for various object detection network models running on the **TCC807x** NPU.
Use the table below to compare inference speed and accuracy across models.

Click on the model name to download a tar file containing the model binary for TCC807x.

---

### 📊 Table Overview

| Column                    | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **Model**                | Name of the neural network model      |
| **Framework**            | Deep learning framework used (e.g., PyTorch, TFLite, ONNX)                  |
| **Dataset**              | Dataset used to benchmark model performance                                                          |
| **Input Size (WxHxC)**   | Input Size (Width × Height × Channels) of the input image required by the model                            |
| **Inference Time (ms)**  | Inference time measured on the TCC807x EVB using zero-padded input images                               |
| **mAP**             | Mean Average Precision on the **COCO2017 validation** set (5,000 images) — **FP32** measured on PC, **INT8** on the TCC807x EVB.                    |
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
            <td align="right">4.24</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.389</td> <!-- Evaluation Result: FP32 -->
            <td align="right">0.386</td> <!-- Evaluation Result: INT8 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">2.059</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.031</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">6.724</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/tensorflow/models/blob/f007603b50b4db38907594a156994a4e983d2d31/research/object_detection/g3doc/tf1_detection_zoo.md">GitHub</a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" rowspan="2" class="model"><a href="YOLO/yolov3/README.md">YOLOv3</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolov3/yolov3_tiny/">tiny</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">8.11</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.321</td> <!-- Evaluation Result: FP32 IoU=0.50 -->
            <td align="right">0.305</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">2.040</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.031</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">8.248</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/ultralytics/yolov3">GitHub</a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov3/yolov3/"> - </a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">96.94</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.611</td> <!-- Evaluation Result: FP32 IoU=0.50 -->
            <td align="right">0.558</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">2.374</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.031</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">57.834</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/ultralytics/yolov3">GitHub</a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" rowspan="1" class="model"><a href="YOLO/yolov4/README.md">YOLOv4</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolov4/yolov4">-</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">608x608x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">52.17</td>
            <td align="right">0.609</td>
            <td align="right">0.592</td>
            <td align="center">INT8</td>
            <td align="right">2.378</td>
            <td align="right">0.031</td>
            <td align="right">61.595</td>
            <td align="center"><a href="https://github.com/AlexeyAB/darknet">GitHub</a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" rowspan="5" class="model"><a href="YOLO/yolov5/README.md">YOLOv5</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolov5/yolov5n/">n</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">30.99</td>
            <td align="right">0.418</td>
            <td align="right">0.251</td>
            <td align="center">INT8</td>
            <td align="right">2.462</td>
            <td align="right">0.031</td>
            <td align="right">2.236</td>
            <td align="center" rowspan="5"><a href="https://github.com/ultralytics/yolov5">GitHub</a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov5/yolov5s/">s</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">39.28</td>
            <td align="right">0.520</td>
            <td align="right">0.506</td>
            <td align="center">INT8</td>
            <td align="right">2.462</td>
            <td align="right">0.031</td>
            <td align="right">7.529</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov5/yolov5m/">m</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">56.70</td>
            <td align="right">0.584</td>
            <td align="right">0.572</td>
            <td align="center">INT8</td>
            <td align="right">2.462</td>
            <td align="right">0.031</td>
            <td align="right">20.845</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov5/yolov5l/">l</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">81.37</td>
            <td align="right">0.615</td>
            <td align="right">0.607</td>
            <td align="center">INT8</td>
            <td align="right">2.460</td>
            <td align="right">0.031</td>
            <td align="right">44.966</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov5/yolov5x/">x</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">115.67</td>
            <td align="right">0.628</td>
            <td align="right">0.620</td>
            <td align="center">INT8</td>
            <td align="right">2.462</td>
            <td align="right">0.031</td>
            <td align="right">82.275</td>
        </tr>
        <tr>
            <td align="center" rowspan="4" class="model"><a href="YOLO/yolov6/README.md">YOLOv6</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolov6/yolov6n/">n</a></td> <!-- Models: Variant -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">12.40</td>
            <td align="right">0.482</td>
            <td align="right">0.346</td>
            <td align="center">INT8</td>
            <td align="right">2.351</td>
            <td align="right">0.031</td>
            <td align="right">3.076</td>
            <td align="center" rowspan="4"><a href="https://github.com/meituan/YOLOv6">GitHub</a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov6/yolov6s/">s</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">17.36</td>
            <td align="right">0.562</td>
            <td align="right">0.409</td>
            <td align="center">INT8</td>
            <td align="right">2.352</td>
            <td align="right">0.031</td>
            <td align="right">10.103</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov6/yolov6m/">m</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">25.53</td>
            <td align="right">0.581</td>
            <td align="right">0.535</td>
            <td align="center">INT8</td>
            <td align="right">2.351</td>
            <td align="right">0.031</td>
            <td align="right">18.115</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov6/yolov6l/">l</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">73.49</td>
            <td align="right">0.625</td>
            <td align="right">0.586</td>
            <td align="center">INT8</td>
            <td align="right">2.352</td>
            <td align="right">0.031</td>
            <td align="right">41.388</td>
        </tr>
        <tr>
            <td align="center" rowspan="2" class="model"><a href="YOLO/yolov7/README.md">YOLOv7</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolov7/yolov7_tiny/">tiny</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">27.24</td>
            <td align="right">0.502</td>
            <td align="right">0.489</td>
            <td align="center">INT8</td>
            <td align="right">2.435</td>
            <td align="right">0.031</td>
            <td align="right">4.650</td>
            <td align="center" rowspan="2"><a href="https://github.com/WongKinYiu/yolov7">GitHub</a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov7/yolov7/">-</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">83.11</td>
            <td align="right">0.636</td>
            <td align="right">0.616</td>
            <td align="center">INT8</td>
            <td align="right">2.348</td>
            <td align="right">0.031</td>
            <td align="right">24.127</td>
        </tr>
        <tr>
            <td align="center" rowspan="5" class="model"><a href="YOLO/yolov8/README.md">YOLOv8</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolov8/yolov8n/">n</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">23.93</td>
            <td align="right">0.478</td>
            <td align="right">0.440</td>
            <td align="center">INT8</td>
            <td align="right">2.346</td>
            <td align="right">0.031</td>
            <td align="right">3.494</td>
            <td align="center" rowspan="5"><a href="https://github.com/ultralytics/ultralytics">GitHub</a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov8/yolov8s/">s</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">34.01</td>
            <td align="right">0.558</td>
            <td align="right">0.541</td>
            <td align="center">INT8</td>
            <td align="right">2.349</td>
            <td align="right">0.031</td>
            <td align="right">11.142</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov8/yolov8m/">m</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">52.57</td>
            <td align="right">0.607</td>
            <td align="right">0.584</td>
            <td align="center">INT8</td>
            <td align="right">2.347</td>
            <td align="right">0.031</td>
            <td align="right">25.029</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov8/yolov8l/">l</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">78.75</td>
            <td align="right">0.632</td>
            <td align="right">0.601</td>
            <td align="center">INT8</td>
            <td align="right">2.349</td>
            <td align="right">0.031</td>
            <td align="right">41.818</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov8/yolov8x/">x</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">102.03</td>
            <td align="right">0.641</td>
            <td align="right">0.610</td>
            <td align="center">INT8</td>
            <td align="right">2.348</td>
            <td align="right">0.031</td>
            <td align="right">64.134</td>
        </tr>
        <tr>
            <td align="center" rowspan="1" class="model"><a href="YOLO/yolov9/README.md">YOLOv9</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolov9/yolov9s/">s</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">40.84</td>
            <td align="right">0.570</td>
            <td align="right">0.345</td>
            <td align="center">INT8</td>
            <td align="right">2.373</td>
            <td align="right">0.031</td>
            <td align="right">8.291</td>
            <td align="center"><a href="https://github.com/WongKinYiu/yolov9">GitHub</a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" rowspan="6" class="model"><a href="YOLO/yolox/README.md">YOLOX</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolox/yolox_nano/">nano</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">11.29</td>
            <td align="right">0.302</td>
            <td align="right">0.038</td>
            <td align="center">INT8</td>
            <td align="right">2.334</td>
            <td align="right">0.031</td>
            <td align="right">1.478</td>
            <td align="center" rowspan="6"><a href="https://github.com/Megvii-BaseDetection/YOLOX">GitHub</a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolox/yolox_tiny/">tiny</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">13.11</td>
            <td align="right">0.381</td>
            <td align="right">0.362</td>
            <td align="center">INT8</td>
            <td align="right">2.334</td>
            <td align="right">0.031</td>
            <td align="right">5.654</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolox/yolox_s/">s</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">30.97</td>
            <td align="right">0.465</td>
            <td align="right">0.447</td>
            <td align="center">INT8</td>
            <td align="right">2.335</td>
            <td align="right">0.031</td>
            <td align="right">9.404</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolox/yolox_m/">m</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">52.01</td>
            <td align="right">0.527</td>
            <td align="right">0.507</td>
            <td align="center">INT8</td>
            <td align="right">2.332</td>
            <td align="right">0.031</td>
            <td align="right">25.244</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolox/yolox_l/">l</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">82.25</td>
            <td align="right">0.552</td>
            <td align="right">0.527</td>
            <td align="center">INT8</td>
            <td align="right">2.334</td>
            <td align="right">0.031</td>
            <td align="right">53.275</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolox/yolox_x/">x</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">123.34</td>
            <td align="right">0.568</td>
            <td align="right">0.556</td>
            <td align="center">INT8</td>
            <td align="right">2.334</td>
            <td align="right">0.031</td>
            <td align="right">95.998</td>
        </tr>
    </tbody>
</table>

- - -

### Footnote
* All models in this repository are distributed exclusively as a compiled `.tar` archive for the TCC807x.
* The source models (PyTorch®, ONNX™, and TensorFlow Lite®) are not provided.
