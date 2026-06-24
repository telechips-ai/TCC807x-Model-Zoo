# YOLOv8 Benchmark on TCC807x
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
            <td align="center" rowspan="5" class="model">YOLOv8</td> <!-- Model -->
            <td align="center" class="variant"><a href="yolov8n/">n</a></td>
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
            <td align="center" class="variant"><a href="yolov8s/">s</a></td>
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
            <td align="center" class="variant"><a href="yolov8m/">m</a></td>
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
            <td align="center" class="variant"><a href="yolov8l/">l</a></td>
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
            <td align="center" class="variant"><a href="yolov8x/">x</a></td>
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
    </tbody>
</table>