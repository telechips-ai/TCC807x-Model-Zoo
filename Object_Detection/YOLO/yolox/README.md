# YOLOX Benchmark on TCC807x
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
            <td align="center" rowspan="6" class="model">YOLOX</a></td> <!-- Model -->
            <td align="center" class="variant"><a href="yolox_nano/">nano</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">14.28</td>
            <td align="right">0.172</td>
            <td align="right">0.034</td>
            <td align="right">0.282</td>
            <td align="right">0.059</td>
            <td align="center">INT8</td>
            <td align="right">6.668</td>
            <td align="right">0.032</td>
            <td align="right">1.409</td>
            <td align="center" rowspan="6"><a href="https://github.com/Megvii-BaseDetection/YOLOX">GitHub<a></td> <!-- References: Link -->
            <td align="center" rowspan="6">Apache-2.0</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolox_tiny/">tiny</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">416x416x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">14.87</td>
            <td align="right">0.205</td>
            <td align="right">0.157</td>
            <td align="right">0.336</td>
            <td align="right">0.305</td>
            <td align="center">INT8</td>
            <td align="right">6.667</td>
            <td align="right">0.032</td>
            <td align="right">5.702</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolox_s/">s</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">33.83</td>
            <td align="right">0.283</td>
            <td align="right">0.164</td>
            <td align="right">0.429</td>
            <td align="right">0.281</td>
            <td align="center">INT8</td>
            <td align="right">6.659</td>
            <td align="right">0.032</td>
            <td align="right">9.724</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolox_m/">m</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">40.83</td>
            <td align="right">0.329</td>
            <td align="right">0.159</td>
            <td align="right">0.479</td>
            <td align="right">0.257</td>
            <td align="center">INT8</td>
            <td align="right">6.658</td>
            <td align="right">0.032</td>
            <td align="right">26.149</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolox_l/">l</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">51.30</td>
            <td align="right">0.340</td>
            <td align="right">0.229</td>
            <td align="right">0.491</td>
            <td align="right">0.409</td>
            <td align="center">INT8</td>
            <td align="right">6.659</td>
            <td align="right">0.032</td>
            <td align="right">53.568</td>
        </tr>
        <tr>
            <td align="center" class="variant"><a href="yolox_x/">x</a></td>
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">COCO2017</td> <!-- Detections/DataSet -->
            <td align="center">640x640x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">65.62</td>
            <td align="right">0.399</td>
            <td align="right">0.314</td>
            <td align="right">0.563</td>
            <td align="right">0.502</td>
            <td align="center">INT8</td>
            <td align="right">6.659</td>
            <td align="right">0.032</td>
            <td align="right">95.310</td>
        </tr>
    </tbody>
</table>
