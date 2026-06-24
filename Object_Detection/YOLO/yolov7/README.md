# YOLOv7 Benchmark on TCC807x
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
            <td align="center" rowspan="2" class="model">YOLOv7</td> <!-- Model -->
            <td align="center" class="variant"><a href="yolov7_tiny/">tiny</a></td> <!-- Model -->
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
            <td align="center" class="variant"><a href="yolov7/">-</a></td> <!-- Models: Variant -->
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
    </tbody>
</table>
