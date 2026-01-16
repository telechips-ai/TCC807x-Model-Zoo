# YOLOv9 Benchmark on TCC807x
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
            <td align="center" rowspan="1" class="model">YOLOv9</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="yolov9s/">s</a></td> <!-- Models: Variant -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">32.44</td>
            <td align="right">0.239</td>
            <td align="right">0.201</td>
            <td align="right">0.386</td>
            <td align="right">0.328</td>
            <td align="center">INT8</td>
            <td align="right">2.850</td>
            <td align="right">0.032</td>
            <td align="right">8.091</td>
            <td align="center"><a href="https://github.com/WongKinYiu/yolov9">GitHub<a></td> <!-- References: Link -->
            <td align="center">GPL-3.0</td>
        </tr>
    </tbody>
</table>
