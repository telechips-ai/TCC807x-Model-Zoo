# YOLOv6 Benchmark on TCC807x
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
            <td align="center" rowspan="4" class="model">YOLOv6</td> <!-- Model -->
            <td align="center" class="variant"><a href="yolov6n/">n</a></td> <!-- Models: Variant -->
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
            <td align="center" class="variant"><a href="yolov6s/">s</a></td> <!-- Model -->
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
            <td align="center" class="variant"><a href="yolov6m/">m</a></td> <!-- Model -->
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
            <td align="center" class="variant"><a href="yolov6l/">l</a></td> <!-- Model -->
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
    </tbody>
</table>