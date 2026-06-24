# Classification Benchmark on TCC807x
The following table shows benchmark results for various classification models running on the **TCC807x** NPU.
Use the table below to compare inference speed and accuracy across models.

Click on the model name to download a tar file containing the model binary for TCC807x.

- - -

### 📊 Table Overview

| Column                    | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **Model**                | Name of the neural network model    |
| **Framework**            | Deep learning framework used (e.g., PyTorch, TFLite, ONNX)                  |
| **Dataset**              | Dataset used to benchmark model performance  |
| **Input Size (WxHxC)**   | Input Size (Width × Height × Channels) of the input image required by the model    |
| **Inference Time (ms)**  | Inference time measured on the TCC807x EVB using zero-padded input images                |
| **Accuracy**             | Top-1 classification accuracy on each model's evaluation dataset (e.g., **ImageNet validation** set, 50,000 images; **MNIST test** set, 10,000 images) — **FP32** measured on PC, **INT8** on the TCC807x EVB.                    |
| **Quantization Bit**     | Bit-depth used for quantization (e.g., INT8)                                |
| **Compiled Model Files**   | Sizes of the compiled model components: .json, .params, and .so for execution on TCC807x                     |
| **References**           | Link to the original GitHub repository of the model

- - -

<table border="1" cellspacing="0" cellpadding="5">
    <thead>
        <tr>
            <th rowspan="2" colspan="2">Model</th>
            <th rowspan="2">Framework</th>
            <th rowspan="2">Dataset</th>
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
            <td align="center" colspan="1"><a href="EfficientNet/README.md">EfficientNet</a></td>
            <td align="center"><a href="EfficientNet/efficientnet_lite0/">Lite0</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">ILSVRC 2012</td> <!-- Detections/DataSet -->
            <td align="center">224x224x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">1.75</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.751</td> <!-- Evaluation Result: FP32 -->
            <td align="right">0.749</td> <!-- Evaluation Result: INT8 -->
            <td align="center">UINT8</td> <!-- Quantization Bit -->
            <td align="right">2.868</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.092</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">5.311</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/tensorflow/tpu/tree/master/models/official/efficientnet/lite">GitHub</a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" colspan="1" rowspan="1"><a href="MobileNet/README.md">MobileNet-v2</a></td>
            <td align="center"><a href="MobileNet/mobilenet_v2_1.0/">1.0</a></td> <!-- Model -->
            <td align="center">TFLite</td> <!-- Framework -->
            <td align="center">ILSVRC 2012</td> <!-- Detections/DataSet -->
            <td align="center">224x224x3</td> <!-- Input Size (WxHxC) -->
            <td align="right">1.52</td> <!-- Inference Time(msec): EVB -->
            <td align="right">0.718</td> <!-- Evaluation Result: FP32 -->
            <td align="right">0.712</td> <!-- Evaluation Result: INT8 -->
            <td align="center">INT8</td> <!-- Quantization Bit -->
            <td align="right">2.743</td> <!-- Compiled NN Information: Graph file (.json) (KB) -->
            <td align="right">0.031</td> <!-- Compiled NN Information: weight & bias (.params) (KB) -->
            <td align="right">3.906</td> <!-- Compiled NN Information: Network (.so) (MB) -->
            <td align="center"><a href="https://github.com/openvinotoolkit/open_model_zoo/tree/master/models/public/mobilenet-v2-1.0-224">GitHub</a></td> <!-- References: Link -->
        </tr>
        <tr>
            <td align="center" colspan="1" rowspan="1"><a href="ResNet/README.md">ResNet</a></td>
            <td align="center"><a href="ResNet/ResNet50-v2/">50-v2</a></td> <!-- Model -->
            <td align="center">TFLite</td>
            <td align="center">ILSVRC 2012</td>
            <td align="center">224x224x3</td>
            <td align="right">5.02</td>
            <td align="right">0.735</td> <!-- FP32 -->
            <td align="right">0.704</td> <!-- INT8 -->
            <td align="center">INT8</td>
            <td align="right">1.753</td> <!-- .json KB -->
            <td align="right">0.031</td> <!-- .params KB -->
            <td align="right">18.228</td> <!-- .so MB -->
            <td align="center"><a href="https://github.com/onnx/models/tree/main/validated/vision/classification/resnet">GitHub</a></td> <!-- References -->
        </tr>
        <tr>
            <td align="center" colspan="1" rowspan="1"><a href="LeNet/README.md">LeNet5</a></td>
            <td align="center"><a href="LeNet/LeNet5/">-</a></td>
            <td align="center">TFLite</td>
            <td align="center">MNIST</td>
            <td align="center">32x32x1</td>
            <td align="right">0.25</td>
            <td align="right">0.984</td> <!-- FP32 -->
            <td align="right">0.985</td> <!-- INT8 -->
            <td align="center">INT8</td>
            <td align="right">1.771</td> <!-- .json KB -->
            <td align="right">0.031</td> <!-- .params KB -->
            <td align="right">0.103</td> <!-- .so MB -->
            <td align="center"><a href="https://huggingface.co/mindspore-ai/LeNet">HuggingFace</a></td> <!-- References -->
        </tr>
    </tbody>
</table>

- - -

### Footnote
* All models in this repository are distributed exclusively as a compiled `.tar` archive for the TCC807x.
* The source models (PyTorch®, ONNX™, and TensorFlow Lite®) are not provided.
