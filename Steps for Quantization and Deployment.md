# Quantization

For this project, Quantization Aware Training was carried out on Kaggle Notebooks as there are various GPUs available for use.
Also, Tensorflow was used as the preferred framework to create models and carry out inferencing.

Here are a few points that should be followed before attempting quantization aware training of a model.
- Make use of GPUs available as Kaggle Notebooks or it will throw error everytime quantization needs to happen.
- Also, few chances are the GPU selected might not support quantization aware training. So, a good idea is to iterate through available GPUs.
- For this project, GPU T4 x2 type of accelerator was used.
- There are a few layers that aren't supported while training and hence, one needs to be mindful about them and select those that quantize.
  For e.g. BatchNormalization, Depthwise separable convolutions are some layers that do not quantize in current version of tensorflow.
- Model was converted to its corresponding tflite version and then downloaded into the local machine to transfer over to edge machine.

# Deployment

The tflite model downloaded, was transferred to an edge computing board called Raspberry Pi 3B+ on headless mode using WinSCP.

