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
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">47.32</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.436</td> <!-- Evaluation Result: FP32 IoU=0.50 -->
            <td align="right">0.426</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">2.520</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.032</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">56.952</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/ultralytics/yolov3">Github<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov3/yolov3_tiny/">tiny</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">5.25</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.260</td> <!-- Evaluation Result: FP32 IoU=0.50 -->
            <td align="right">0.215</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">2.158</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.032</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">7.612</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/ultralytics/yolov3">Github<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" rowspan="1" class="model"><a href="YOLO/yolov4/README.md">YOLOv4</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolov4/yolov4">-</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">608x608x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">47.51</td>
            <td align="right">0.476</td>
            <td align="right">0.446</td>
            <td align="center">INT8</td>
            <td align="right">2.435</td>
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
            <td align="right">11.47</td>
            <td align="right">0.382</td>
            <td align="right">0.328</td>
            <td align="center">INT8</td>
            <td align="right">2.459</td>
            <td align="right">0.032</td>
            <td align="right">4.806</td>
            <td align="center" rowspan="4"><a href="https://github.com/meituan/YOLOv6">GitHub<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov6/yolov6s/">s</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">14.52</td>
            <td align="right">0.442</td>
            <td align="right">0.352</td>
            <td align="center">INT8</td>
            <td align="right">2.462</td>
            <td align="right">0.032</td>
            <td align="right">17.270</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov6/yolov6m/">m</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">20.79</td>
            <td align="right">0.451</td>
            <td align="right">0.424</td>
            <td align="center">INT8</td>
            <td align="right">2.459</td>
            <td align="right">0.032</td>
            <td align="right">31.828</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov6/yolov6l/">l</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">29.90</td>
            <td align="right">0.456</td>
            <td align="right">0.427</td>
            <td align="center">INT8</td>
            <td align="right">2.458</td>
            <td align="right">0.032</td>
            <td align="right">58.312</td>
        </tr>
        <tr>
            <td align="center" rowspan="2" class="model"><a href="YOLO/yolov7/README.md">YOLOv7</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolov7/yolov7/">-</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">41.39</td>
            <td align="right">0.474</td>
            <td align="right">0.459</td>
            <td align="center">INT8</td>
            <td align="right">2.494</td>
            <td align="right">0.032</td>
            <td align="right">36.022</td>
            <td align="center" rowspan="2"><a href="https://github.com/WongKinYiu/yolov7">GitHub<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov7/yolov7_tiny/">tiny</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">27.62</td>
            <td align="right">0.404</td>
            <td align="right">0.381</td>
            <td align="center">INT8</td>
            <td align="right">2.494</td>
            <td align="right">0.032</td>
            <td align="right">6.637</td>
        </tr>
        <tr>
            <td align="center" rowspan="5" class="model"><a href="YOLO/yolov8/README.md">YOLOv8</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolov8/yolov8n/">n</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">18.44</td>
            <td align="right">0.369</td>
            <td align="right">0.347</td>
            <td align="center">INT8</td>
            <td align="right">1.758</td>
            <td align="right">0.032</td>
            <td align="right">3.577</td>
            <td align="center" rowspan="5"><a href="https://github.com/ultralytics/ultralytics">GitHub<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov8/yolov8s/">s</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">21.73</td>
            <td align="right">0.417</td>
            <td align="right">0.391</td>
            <td align="center">INT8</td>
            <td align="right">1.813</td>
            <td align="right">0.032</td>
            <td align="right">8.321</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov8/yolov8m/">m</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">28.00</td>
            <td align="right">0.455</td>
            <td align="right">0.435</td>
            <td align="center">INT8</td>
            <td align="right">1.813</td>
            <td align="right">0.032</td>
            <td align="right">18.237</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov8/yolov8l/">l</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">36.92</td>
            <td align="right">0.478</td>
            <td align="right">0.450</td>
            <td align="center">INT8</td>
            <td align="right">1.812</td>
            <td align="right">0.032</td>
            <td align="right">29.775</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolov8/yolov8x/">x</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">46.21</td>
            <td align="right">0.481</td>
            <td align="right">0.456</td>
            <td align="center">INT8</td>
            <td align="right">1.813</td>
            <td align="right">0.032</td>
            <td align="right">45.213</td>
        </tr>
        <tr>
            <td align="center" rowspan="1" class="model"><a href="YOLO/yolov9/README.md">YOLOv9</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolov9/yolov9s/">s</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">32.44</td>
            <td align="right">0.386</td>
            <td align="right">0.328</td>
            <td align="center">INT8</td>
            <td align="right">2.850</td>
            <td align="right">0.032</td>
            <td align="right">8.091</td>
            <td align="center"><a href="https://github.com/WongKinYiu/yolov9">GitHub<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" rowspan="6" class="model"><a href="YOLO/yolox/README.md">YOLOX</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="YOLO/yolox/yolox_nano/">nano</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">14.28</td>
            <td align="right">0.282</td>
            <td align="right">0.059</td>
            <td align="center">INT8</td>
            <td align="right">6.668</td>
            <td align="right">0.032</td>
            <td align="right">1.409</td>
            <td align="center" rowspan="6"><a href="https://github.com/Megvii-BaseDetection/YOLOX">GitHub<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolox/yolox_tiny/">tiny</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">14.87</td>
            <td align="right">0.336</td>
            <td align="right">0.305</td>
            <td align="center">INT8</td>
            <td align="right">6.667</td>
            <td align="right">0.032</td>
            <td align="right">5.702</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolox/yolox_s/">s</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">33.83</td>
            <td align="right">0.429</td>
            <td align="right">0.281</td>
            <td align="center">INT8</td>
            <td align="right">6.659</td>
            <td align="right">0.032</td>
            <td align="right">9.724</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolox/yolox_m/">m</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">40.83</td>
            <td align="right">0.479</td>
            <td align="right">0.257</td>
            <td align="center">INT8</td>
            <td align="right">6.658</td>
            <td align="right">0.032</td>
            <td align="right">26.149</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolox/yolox_l/">l</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">51.30</td>
            <td align="right">0.491</td>
            <td align="right">0.409</td>
            <td align="center">INT8</td>
            <td align="right">6.659</td>
            <td align="right">0.032</td>
            <td align="right">53.568</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="YOLO/yolox/yolox_x/">x</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">65.62</td>
            <td align="right">0.563</td>
            <td align="right">0.502</td>
            <td align="center">INT8</td>
            <td align="right">6.659</td>
            <td align="right">0.032</td>
            <td align="right">95.310</td>
        </tr>
    </tbody>
</table>

- - -

### Footnote
* All models in this repository are distributed exclusively in TensorFlow Lite® format.
* TFLite® and ONNX™ are not provided.
