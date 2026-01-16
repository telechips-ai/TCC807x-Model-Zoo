# YOLOv8 Benchmark on TCC807x
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
            <td align="center" rowspan="5" class="model">YOLOv8</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="yolov8n/">n</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">18.44</td>
            <td align="right">0.260</td>
            <td align="right">0.240</td>
            <td align="right">0.369</td>
            <td align="right">0.347</td>
            <td align="center">INT8</td>
            <td align="right">1.758</td>
            <td align="right">0.032</td>
            <td align="right">3.577</td>
            <td align="center" rowspan="5"><a href="https://github.com/ultralytics/ultralytics">GitHub<a></td> <!-- References: Link -->
            <td align="center" rowspan="5">AGPL-3.0</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov8s/">s</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">21.73</td>
            <td align="right">0.301</td>
            <td align="right">0.280</td>
            <td align="right">0.417</td>
            <td align="right">0.391</td>
            <td align="center">INT8</td>
            <td align="right">1.813</td>
            <td align="right">0.032</td>
            <td align="right">8.321</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov8m/">m</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">28.00</td>
            <td align="right">0.340</td>
            <td align="right">0.322</td>
            <td align="right">0.455</td>
            <td align="right">0.435</td>
            <td align="center">INT8</td>
            <td align="right">1.813</td>
            <td align="right">0.032</td>
            <td align="right">18.237</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov8l/">l</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">36.92</td>
            <td align="right">0.363</td>
            <td align="right">0.338</td>
            <td align="right">0.478</td>
            <td align="right">0.450</td>
            <td align="center">INT8</td>
            <td align="right">1.812</td>
            <td align="right">0.032</td>
            <td align="right">29.775</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov8x/">x</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">46.21</td>
            <td align="right">0.365</td>
            <td align="right">0.345</td>
            <td align="right">0.481</td>
            <td align="right">0.456</td>
            <td align="center">INT8</td>
            <td align="right">1.813</td>
            <td align="right">0.032</td>
            <td align="right">45.213</td>
        </tr>
    </tbody>
</table>