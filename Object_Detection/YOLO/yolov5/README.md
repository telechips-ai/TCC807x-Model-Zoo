# YOLOv5 Benchmark on TCC807x
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
            <td align="center" rowspan="5" class="model">YOLOv5</td> <!-- Model -->
            <td align="center" class="variant"><a href="yolov5n/">n</a></td>
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
            <td align="center" class="variant"><a href="yolov5s/">s</a></td>
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
            <td align="center" class="variant"><a href="yolov5m/">m</a></td>
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
            <td align="center" class="variant"><a href="yolov5l/">l</a></td>
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
            <td align="center" class="variant"><a href="yolov5x/">x</a></td>
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
    </tbody>
</table>
