# Classification Benchmark on TCC807x
The following table shows benchmark results for various Classification models running on the **TCC807x** NPU.  
You can compare the performance of each model.  

Click on the model name to download a tar file containing the model binary for TCC807x.

- - -

### 📊 Table Overview

| Column                    | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **Model**                | Name of the image classification model    |
| **Framework**            | Deep learning framework used (e.g., PyTorch, TFLite, ONNX)                  |
| **Dataset**              | Dataset used to benchmark model performance  |
| **Input Size (WxHxC)**   | Input Size (Width × Height × Channels) of the input image required by the model    |
| **Inference Time (ms)**  | Inference time measured on the TCC807x EVB using zero-padded input images                |
| **Accuracy**             | Top-1 classification accuracy on the ImageNet validation dataset (50,000 images)                    |
| **Quantization Bit**     | Bit-depth used for quantization (e.g., INT8)                                |
| **Compiled Model Files**   | Sizes of the compiled model components: .json, .params, and .so for execution on TCC807x                     |
| **References**           | Link to the original GitHub repository of the model      

- - -

<table border="1" cellspacing="0" cellpadding="5">
    <thead>
        <tr>
            <th rowspan="2" colspan="2">Model</th>
            <th rowspan="2">Framework</th>
            <th rowspan="2">DataSet</th>
            <th rowspan="2">Input Size (WxHxC)</th>
            <th rowspan="2">Inference Time (ms)</th>
            <th colspan="2">Accuracy</th>
            <th rowspan="2">Quantization Bit</th>
            <th colspan="3">Compiled Model Files</th>
            <th rowspan="2">References</th>
        </tr>
        <tr>
            <th>FP32</th>
            <th>INT8</th>
            <th>.json (KB)</th>
            <th>.params (KB)</th>
            <th>.so (MB)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center" colspan="1"><a href="EfficientNet/README.md">EfficientNet</td>
            <td align="center"><a href="EfficientNet/efficientnet_lite0/">Lite0</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">ILSVRC 2012</td> <!-- Detections/DataSet -->
            <td align="center">224x224x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">1.49</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.751</td> <!-- Evaluation Result: FP32 -->
            <td align="right">0.725</td> <!-- Evaluation Result: INT8 -->
            <td align="center">UINT8</td> <!-- Quantization Bit -->
            <td align="right">17.36</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.75</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">5</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/tensorflow/tpu/tree/master/models/official/efficientnet/lite">Github<a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" colspan="1" rowspan="1"><a href="MobileNet/README.md">MobileNet-v2</a></td>
            <td align="center"><a href="MobileNet/mobilenet_v2_1.4/">1.4</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">ILSVRC 2012</td> <!-- Detections/DataSet -->
            <td align="center">224x224x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">1.16</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.719</td> <!-- Evaluation Result: FP32 -->
            <td align="right">0.712</td> <!-- Evaluation Result: INT8 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">16.36</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.25</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">32</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/openvinotoolkit/open_model_zoo/tree/master/models/public/mobilenet-v2-1.4-224">Github<a></td> <!-- References: Link -->
        </tr>
    </tbody>
</table>

- - -

### Footnote                
* All models in this repository are distributed exclusively in TensorFlow Lite® format.  
* PyTorch® and ONNX™ are not provided.
