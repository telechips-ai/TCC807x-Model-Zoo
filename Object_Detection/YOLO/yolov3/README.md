# YOLOv3 Benchmark on TCC807x
---
<table border="1" cellspacing="0" cellpadding="5">
    <thead>
        <tr>
            <th align="center" rowspan="2" colspan="2">Model</th>
            <th th align="center" rowspan="2">Framework</th>
            <th th align="center" rowspan="2">Dataset</th>
            <th th align="center" rowspan="2">Input Size (WxHxC)</th>
            <th th align="center" rowspan="2">Inference Time (ms)</th>
            <th th align="center" colspan="2">mAP@50:95</th>
            <th th align="center" colspan="2">mAP@50</th>
            <th th align="center" rowspan="2">Quantization Bit</th>
            <th th align="center" colspan="3">Compiled Model Files</th>
            <th th align="center" colspan="2">References</th>
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
            <td align="center" colspan="2"><a href="yolov3/">YOLOv3</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">47.32</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.305</td> <!-- Evaluation Result: FP32 IoU=0.50:0.95 -->
            <td align="right">0.261</td> <!-- Evaluation Result: INT8 IoU=0.50:0.95 -->
            <td align="right">0.436</td> <!-- Evaluation Result: FP32 IoU=0.50 -->
            <td align="right">0.426</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">2.520</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.032</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">56.952</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/ultralytics/yolov3">Github<a></td> <!-- References: Link -->
            <td align="center">AGPL-3.0</td>
        </tr>
        <tr>
            <td align="center" colspan="2"><a href="yolov3_tiny/">YOLOv3-tiny</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">5.25</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.136</td> <!-- Evaluation Result: FP32 IoU=0.50:0.95 -->
            <td align="right">0.104</td> <!-- Evaluation Result: INT8 IoU=0.50:0.95 -->
            <td align="right">0.260</td> <!-- Evaluation Result: FP32 IoU=0.50 -->
            <td align="right">0.215</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">2.158</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.032</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">7.612</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/ultralytics/yolov3">Github<a></td> <!-- References: Link -->
            <td align="center">AGPL-3.0</td>
        </tr>
    </tbody>
</table>