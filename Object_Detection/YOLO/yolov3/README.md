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
            <th>.json(KB)</th>
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
            <td align="right">15.21</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.387</td> <!-- Evaluation Result: FP32 IoU=0.50:0.95 -->
            <td align="right">0.345</td> <!-- Evaluation Result: INT8 IoU=0.50:0.95 -->
            <td align="right">0.588</td> <!-- Evaluation Result: FP32 IoU=0.50 -->
            <td align="right">0.560</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">29.52</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">1.74</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">470</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/ultralytics/yolov3">Github<a></td> <!-- References: Link -->
            <td align="center">AGPL-3.0</td>
        </tr>
        <tr>
            <td align="center" colspan="2"><a href="yolov3-tiny/">YOLOv3-tiny</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">2.50</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.172</td> <!-- Evaluation Result: FP32 IoU=0.50:0.95 -->
            <td align="right">0.152</td> <!-- Evaluation Result: INT8 IoU=0.50:0.95 -->
            <td align="right">0.338</td> <!-- Evaluation Result: FP32 IoU=0.50 -->
            <td align="right">0.319</td> <!-- Evaluation Result: INT8 IoU=0.50 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">17.62</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.25</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">63</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/ultralytics/yolov3">Github<a></td> <!-- References: Link -->
            <td align="center">AGPL-3.0</td>
        </tr>
    </tbody>
</table>