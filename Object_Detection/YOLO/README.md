# YOLO Series Benchmark on TCC807x

The following table shows benchmark results for various YOLO (You Only Look Once) object detection models running on the **TCC807x** NPU.
YOLO models are widely known for their real-time performance and high accuracy in detecting multiple objects in a single pass over the image.

Click on the model name to download a tar file containing the model binary for TCC807x.

---

### 📊 Table Overview

| Column                    | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **Model**                | Name of the neural network model     |
| **Framework**            | Deep learning framework used (e.g., PyTorch, TFLite, ONNX)                  |
| **Dataset**              | Dataset used to benchmark model performance                                                           |
| **Input Size (WxHxC)**   | Input Size (Width × Height × Channels) of the input image required by the model                            |
| **Inference Time (ms)**  | Inference time measured on the TCC807x EVB using zero-padded input images                               |
| **mAP**             | Mean Average Precision evaluated on the **COCO2017 validation** set (5,000 images) — **FP32** measured on PC, **INT8** on the TCC807x EVB.                 |
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
            <td align="center" rowspan="2" class="model">YOLOv3</td> <!-- Model -->
            <td align="center" class="variant"><a href="yolov3/yolov3_tiny/">tiny</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">8.11</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.168</td> <!-- Evaluation Result: FP32 IoU=0.50:0.95 -->
            <td align="right">0.147</td> <!-- Evaluation Result: INT8 IoU=0.50:0.95 -->
            <td align="right">0.321</td> <!-- Evaluation Result: FP32 IoU=0.50 -->
            <td align="right">0.305</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">2.040</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.031</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">8.248</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/ultralytics/yolov3">GitHub</a></td> <!-- References: Link -->
            <td align="center">AGPL-3.0</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov3/yolov3/">-</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">96.94</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.427</td> <!-- Evaluation Result: FP32 IoU=0.50:0.95 -->
            <td align="right">0.349</td> <!-- Evaluation Result: INT8 IoU=0.50:0.95 -->
            <td align="right">0.611</td> <!-- Evaluation Result: FP32 IoU=0.50 -->
            <td align="right">0.558</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">2.374</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.031</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">57.834</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/ultralytics/yolov3">GitHub</a></td> <!-- References: Link -->
            <td align="center">AGPL-3.0</td>
        </tr>
        <tr>
            <td align="center" colspan="2"><a href="yolov4/yolov4/">YOLOv4</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">608x608x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">52.17</td>
            <td align="right">0.400</td>
            <td align="right">0.329</td>
            <td align="right">0.609</td>
            <td align="right">0.592</td>
            <td align="center">INT8</td>
            <td align="right">2.378</td>
            <td align="right">0.031</td>
            <td align="right">61.595</td>
            <td align="center"><a href="https://github.com/AlexeyAB/darknet">GitHub</a></td> <!-- References: Link -->
            <td align="center">Public Domain</td>
        </tr>
        <tr>
            <td align="center" rowspan="5" class="model"><a href="yolov5/README.md">YOLOv5</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="yolov5/yolov5n/">n</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">30.99</td>
            <td align="right">0.248</td>
            <td align="right">0.141</td>
            <td align="right">0.418</td>
            <td align="right">0.251</td>
            <td align="center">INT8</td>
            <td align="right">2.462</td>
            <td align="right">0.031</td>
            <td align="right">2.236</td>
            <td align="center" rowspan="5"><a href="https://github.com/ultralytics/yolov5">GitHub</a></td> <!-- References: Link -->
            <td align="center" rowspan="5">AGPL-3.0</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov5/yolov5s/">s</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">39.28</td>
            <td align="right">0.332</td>
            <td align="right">0.301</td>
            <td align="right">0.520</td>
            <td align="right">0.506</td>
            <td align="center">INT8</td>
            <td align="right">2.462</td>
            <td align="right">0.031</td>
            <td align="right">7.529</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov5/yolov5m/">m</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">56.70</td>
            <td align="right">0.398</td>
            <td align="right">0.364</td>
            <td align="right">0.584</td>
            <td align="right">0.572</td>
            <td align="center">INT8</td>
            <td align="right">2.462</td>
            <td align="right">0.031</td>
            <td align="right">20.845</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov5/yolov5l/">l</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">81.37</td>
            <td align="right">0.433</td>
            <td align="right">0.403</td>
            <td align="right">0.615</td>
            <td align="right">0.607</td>
            <td align="center">INT8</td>
            <td align="right">2.460</td>
            <td align="right">0.031</td>
            <td align="right">44.966</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov5/yolov5x/">x</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">115.67</td>
            <td align="right">0.447</td>
            <td align="right">0.416</td>
            <td align="right">0.628</td>
            <td align="right">0.620</td>
            <td align="center">INT8</td>
            <td align="right">2.462</td>
            <td align="right">0.031</td>
            <td align="right">82.275</td>
        </tr>
        <tr>
            <td align="center" rowspan="4" class="model">YOLOv6</td> <!-- Model -->
            <td align="center" class="variant"><a href="yolov6/yolov6n/">n</a></td> <!-- Models: Variant -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">12.40</td>
            <td align="right">0.328</td>
            <td align="right">0.212</td>
            <td align="right">0.482</td>
            <td align="right">0.346</td>
            <td align="center">INT8</td>
            <td align="right">2.351</td>
            <td align="right">0.031</td>
            <td align="right">3.076</td>
            <td align="center" rowspan="4"><a href="https://github.com/meituan/YOLOv6">GitHub</a></td> <!-- References: Link -->
            <td align="center" rowspan="4">GPL-3.0</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov6/yolov6s/">s</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">17.36</td>
            <td align="right">0.394</td>
            <td align="right">0.257</td>
            <td align="right">0.562</td>
            <td align="right">0.409</td>
            <td align="center">INT8</td>
            <td align="right">2.352</td>
            <td align="right">0.031</td>
            <td align="right">10.103</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov6/yolov6m/">m</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">25.53</td>
            <td align="right">0.410</td>
            <td align="right">0.352</td>
            <td align="right">0.581</td>
            <td align="right">0.535</td>
            <td align="center">INT8</td>
            <td align="right">2.351</td>
            <td align="right">0.031</td>
            <td align="right">18.115</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov6/yolov6l/">l</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">73.49</td>
            <td align="right">0.448</td>
            <td align="right">0.374</td>
            <td align="right">0.625</td>
            <td align="right">0.586</td>
            <td align="center">INT8</td>
            <td align="right">2.352</td>
            <td align="right">0.031</td>
            <td align="right">41.388</td>
        </tr>
        <tr>
            <td align="center" rowspan="2" class="model">YOLOv7</td> <!-- Model -->
            <td align="center" class="variant"><a href="yolov7/yolov7_tiny/">tiny</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">27.24</td>
            <td align="right">0.328</td>
            <td align="right">0.292</td>
            <td align="right">0.502</td>
            <td align="right">0.489</td>
            <td align="center">INT8</td>
            <td align="right">2.435</td>
            <td align="right">0.031</td>
            <td align="right">4.650</td>
            <td align="center" rowspan="2"><a href="https://github.com/WongKinYiu/yolov7">GitHub</a></td> <!-- References: Link -->
            <td align="center" rowspan="2">GPL-3.0</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov7/yolov7/">-</a></td> <!-- Models: Variant -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">83.11</td>
            <td align="right">0.452</td>
            <td align="right">0.388</td>
            <td align="right">0.636</td>
            <td align="right">0.616</td>
            <td align="center">INT8</td>
            <td align="right">2.348</td>
            <td align="right">0.031</td>
            <td align="right">24.127</td>
        </tr>
        <tr>
            <td align="center" rowspan="5" class="model">YOLOv8</td> <!-- Model -->
            <td align="center" class="variant"><a href="yolov8/yolov8n/">n</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">23.93</td>
            <td align="right">0.326</td>
            <td align="right">0.292</td>
            <td align="right">0.478</td>
            <td align="right">0.440</td>
            <td align="center">INT8</td>
            <td align="right">2.346</td>
            <td align="right">0.031</td>
            <td align="right">3.494</td>
            <td align="center" rowspan="5"><a href="https://github.com/ultralytics/ultralytics">GitHub</a></td> <!-- References: Link -->
            <td align="center" rowspan="5">AGPL-3.0</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov8/yolov8s/">s</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">34.01</td>
            <td align="right">0.392</td>
            <td align="right">0.374</td>
            <td align="right">0.558</td>
            <td align="right">0.541</td>
            <td align="center">INT8</td>
            <td align="right">2.349</td>
            <td align="right">0.031</td>
            <td align="right">11.142</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov8/yolov8m/">m</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">52.57</td>
            <td align="right">0.437</td>
            <td align="right">0.412</td>
            <td align="right">0.607</td>
            <td align="right">0.584</td>
            <td align="center">INT8</td>
            <td align="right">2.347</td>
            <td align="right">0.031</td>
            <td align="right">25.029</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov8/yolov8l/">l</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">78.75</td>
            <td align="right">0.462</td>
            <td align="right">0.429</td>
            <td align="right">0.632</td>
            <td align="right">0.601</td>
            <td align="center">INT8</td>
            <td align="right">2.349</td>
            <td align="right">0.031</td>
            <td align="right">41.818</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov8/yolov8x/">x</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">102.03</td>
            <td align="right">0.471</td>
            <td align="right">0.437</td>
            <td align="right">0.641</td>
            <td align="right">0.610</td>
            <td align="center">INT8</td>
            <td align="right">2.348</td>
            <td align="right">0.031</td>
            <td align="right">64.134</td>
        </tr>
        <tr>
            <td align="center" rowspan="1" class="model">YOLOv9</td> <!-- Model -->
            <td align="center" class="variant"><a href="yolov9/yolov9s/">s</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">40.84</td>
            <td align="right">0.406</td>
            <td align="right">0.216</td>
            <td align="right">0.570</td>
            <td align="right">0.345</td>
            <td align="center">INT8</td>
            <td align="right">2.373</td>
            <td align="right">0.031</td>
            <td align="right">8.291</td>
            <td align="center"><a href="https://github.com/WongKinYiu/yolov9">GitHub</a></td> <!-- References: Link -->
            <td align="center">GPL-3.0</td>
        </tr>
        <tr>
            <td align="center" rowspan="6" class="model">YOLOX</td> <!-- Model -->
            <td align="center" class="variant"><a href="yolox/yolox_nano/">nano</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">11.29</td>
            <td align="right">0.185</td>
            <td align="right">0.021</td>
            <td align="right">0.302</td>
            <td align="right">0.038</td>
            <td align="center">INT8</td>
            <td align="right">2.334</td>
            <td align="right">0.031</td>
            <td align="right">1.478</td>
            <td align="center" rowspan="6"><a href="https://github.com/Megvii-BaseDetection/YOLOX">GitHub</a></td> <!-- References: Link -->
            <td align="center" rowspan="6">Apache-2.0</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolox/yolox_tiny/">tiny</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">13.11</td>
            <td align="right">0.244</td>
            <td align="right">0.220</td>
            <td align="right">0.381</td>
            <td align="right">0.362</td>
            <td align="center">INT8</td>
            <td align="right">2.334</td>
            <td align="right">0.031</td>
            <td align="right">5.654</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolox/yolox_s/">s</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">30.97</td>
            <td align="right">0.311</td>
            <td align="right">0.288</td>
            <td align="right">0.465</td>
            <td align="right">0.447</td>
            <td align="center">INT8</td>
            <td align="right">2.335</td>
            <td align="right">0.031</td>
            <td align="right">9.404</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolox/yolox_m/">m</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">52.01</td>
            <td align="right">0.367</td>
            <td align="right">0.341</td>
            <td align="right">0.527</td>
            <td align="right">0.507</td>
            <td align="center">INT8</td>
            <td align="right">2.332</td>
            <td align="right">0.031</td>
            <td align="right">25.244</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolox/yolox_l/">l</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">82.25</td>
            <td align="right">0.394</td>
            <td align="right">0.364</td>
            <td align="right">0.552</td>
            <td align="right">0.527</td>
            <td align="center">INT8</td>
            <td align="right">2.334</td>
            <td align="right">0.031</td>
            <td align="right">53.275</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolox/yolox_x/">x</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">123.34</td>
            <td align="right">0.409</td>
            <td align="right">0.387</td>
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

## 📤 Output Format

- The raw output of a YOLO model is a tensor (or multiple tensors) containing a dense grid of predictions across different spatial locations (and, for anchor-based variants, multiple anchor boxes per location).
- These raw outputs require the following post-processing:
  - Applying sigmoid/softmax activations to normalize outputs
  - Filtering boxes based on confidence thresholds
  - Applying Non-Maximum Suppression (NMS) to remove overlapping boxes

- The final post-processed output includes a list of detected objects, each containing:
  - Class label
  - Confidence score
  - Bounding box coordinates (x_min, y_min, x_max, and y_max)

- The number and format of output tensors may vary slightly depending on the YOLO version (e.g., v5, v6, v8, and YOLOX), but the core structure remains similar.

- - -

### Footnote
* All models in this repository are distributed exclusively as a compiled `.tar` archive for the TCC807x.
* The source models (PyTorch®, ONNX™, and TensorFlow Lite®) are not provided.
* License\**:
  - Telechips Inc. is not responsible for any issues, damages, or losses resulting from the use of code downloaded from GitHub repositories provided by Telechips.
  - The performance results of neural networks (such as mAP or inference time) are not subject to license terms and may be used freely.
  - Any output generated by software execution may or may not be subject to license terms, depending on the contract and intended use of the output.
