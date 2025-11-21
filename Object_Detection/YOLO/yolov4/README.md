# YOLOv4 Benchmark on TCC807x
---
<table border="1" cellspacing="0" cellpadding="5">
    <thead>
        <tr>
            <th align="center" rowspan="2" colspan="1">Model</th>
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
            <td align="center" rowspan="1"><a href="yolov4/">YOLOv4</td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">608x608x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">41.59</td>
            <td align="right">0.327</td>
            <td align="right">0.167</td>
            <td align="right">0.476</td>
            <td align="right">0.252</td>
            <td align="center">INT8</td>
            <td align="right">2.363</td>
            <td align="right">0.032</td>
            <td align="right">63.506</td>
            <td align="center"><a href="https://github.com/AlexeyAB/darknet">Github<a></td> <!-- References: Link -->
            <td align="center">GPL-3.0</td>
        </tr>
    </tbody>
</table>