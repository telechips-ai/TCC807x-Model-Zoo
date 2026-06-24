# YOLOv4 Benchmark on TCC807x
---
<table border="1" cellspacing="0" cellpadding="5">
    <thead>
        <tr>
            <th align="center" rowspan="2" colspan="1">Model</th>
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
            <td align="center" rowspan="1"><a href="yolov4/">YOLOv4</a></td> <!-- Model -->
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
    </tbody>
</table>