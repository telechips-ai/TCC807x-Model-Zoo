# YOLOX Benchmark on TCC807x
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
            <td align="center" rowspan="6" class="model">YOLOX</td> <!-- Model -->
            <td align="center" class="variant"><a href="yolox_nano/">nano</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">11.29</td>
            <td align="right">0.185</td>
            <td align="right">0.021</td>
            <td align="right">0.302</td>
            <td align="right">0.038</td>
            <td align="center">INT8</td>
            <td align="right">2.334</td>
            <td align="right">0.031</td>
            <td align="right">1.478</td>
            <td align="center" rowspan="6"><a href="https://github.com/Megvii-BaseDetection/YOLOX">GitHub</a></td> <!-- References: Link -->
            <td align="center" rowspan="6">Apache-2.0</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolox_tiny/">tiny</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">13.11</td>
            <td align="right">0.244</td>
            <td align="right">0.220</td>
            <td align="right">0.381</td>
            <td align="right">0.362</td>
            <td align="center">INT8</td>
            <td align="right">2.334</td>
            <td align="right">0.031</td>
            <td align="right">5.654</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolox_s/">s</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">30.97</td>
            <td align="right">0.311</td>
            <td align="right">0.288</td>
            <td align="right">0.465</td>
            <td align="right">0.447</td>
            <td align="center">INT8</td>
            <td align="right">2.335</td>
            <td align="right">0.031</td>
            <td align="right">9.404</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolox_m/">m</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">52.01</td>
            <td align="right">0.367</td>
            <td align="right">0.341</td>
            <td align="right">0.527</td>
            <td align="right">0.507</td>
            <td align="center">INT8</td>
            <td align="right">2.332</td>
            <td align="right">0.031</td>
            <td align="right">25.244</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolox_l/">l</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">82.25</td>
            <td align="right">0.394</td>
            <td align="right">0.364</td>
            <td align="right">0.552</td>
            <td align="right">0.527</td>
            <td align="center">INT8</td>
            <td align="right">2.334</td>
            <td align="right">0.031</td>
            <td align="right">53.275</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolox_x/">x</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">123.34</td>
            <td align="right">0.409</td>
            <td align="right">0.387</td>
            <td align="right">0.568</td>
            <td align="right">0.556</td>
            <td align="center">INT8</td>
            <td align="right">2.334</td>
            <td align="right">0.031</td>
            <td align="right">95.998</td>
        </tr>
    </tbody>
</table>
