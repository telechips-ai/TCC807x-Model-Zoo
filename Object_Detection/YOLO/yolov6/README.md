# YOLOv6 Benchmark on TCC807x
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
            <td align="center" rowspan="4" class="model">YOLOv6</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="yolov6n/">n</a></td> <!-- Models: Variant -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">39.39</td>
            <td align="right">0.277</td>
            <td align="right">0.215</td>
            <td align="right">0.389</td>
            <td align="right">0.342</td>
            <td align="center">INT8</td>
            <td align="right">16.348</td>
            <td align="right">0.14</td>
            <td align="right">5.033</td>
            <td align="center" rowspan="4"><a href="https://github.com/meituan/YOLOv6">GitHub<a></td> <!-- References: Link -->
            <td align="center" rowspan="4">GPL-3.0</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov6s/">s</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">60.52</td>
            <td align="right">0.328</td>
            <td align="right">0.246</td>
            <td align="right">0.446</td>
            <td align="right">0.407</td>
            <td align="center">INT8</td>
            <td align="right">16.302</td>
            <td align="right">0.14</td>
            <td align="right">17.468</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov6m/">m</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">83.51</td>
            <td align="right">0.349</td>
            <td align="right">0.241</td>
            <td align="right">0.471</td>
            <td align="right">0.437</td>
            <td align="center">INT8</td>
            <td align="right">16.56</td>
            <td align="right">0.194</td>
            <td align="right">32.138</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov6l/">l</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">1414.80</td>
            <td align="right">0.367</td>
            <td align="right">0.243</td>
            <td align="right">0.488</td>
            <td align="right">0.461</td>
            <td align="center">INT8</td>
            <td align="right">208.664</td>
            <td align="right">2.066</td>
            <td align="right">62.854</td>
        </tr>
    </tbody>
</table>