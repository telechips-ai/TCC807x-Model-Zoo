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
            <td align="right">11.47</td>
            <td align="right">0.269</td>
            <td align="right">0.224</td>
            <td align="right">0.382</td>
            <td align="right">0.328</td>
            <td align="center">INT8</td>
            <td align="right">2.459</td>
            <td align="right">0.032</td>
            <td align="right">4.806</td>
            <td align="center" rowspan="4"><a href="https://github.com/meituan/YOLOv6">GitHub<a></td> <!-- References: Link -->
            <td align="center" rowspan="4">GPL-3.0</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov6s/">s</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">14.52</td>
            <td align="right">0.322</td>
            <td align="right">0.238</td>
            <td align="right">0.442</td>
            <td align="right">0.352</td>
            <td align="center">INT8</td>
            <td align="right">2.462</td>
            <td align="right">0.032</td>
            <td align="right">17.270</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov6m/">m</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">20.79</td>
            <td align="right">0.333</td>
            <td align="right">0.306</td>
            <td align="right">0.451</td>
            <td align="right">0.424</td>
            <td align="center">INT8</td>
            <td align="right">2.459</td>
            <td align="right">0.032</td>
            <td align="right">31.828</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolov6l/">l</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">29.90</td>
            <td align="right">0.337</td>
            <td align="right">0.313</td>
            <td align="right">0.456</td>
            <td align="right">0.427</td>
            <td align="center">INT8</td>
            <td align="right">2.458</td>
            <td align="right">0.032</td>
            <td align="right">58.312</td>
        </tr>
    </tbody>
</table>