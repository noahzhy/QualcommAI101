# Qualcomm AI

## Installation and Login

```bash
pip3 install qai-hub
qai-hub configure --api_token YOUR_API_TOKEN_HERE
```


## Export Qualcomm AI Model

Export a Qualcomm AI model from the hub with quantization options.

```bash
pip install "qai-hub-models[yolov11-det]"
python -m qai_hub_models.models.yolov11_det.export { --quantize w8a8 }
```


## Inference

Check the device which is available for inference.
Recommend using the `qai-hub` CLI to check the available devices.

```bash
qai-hub list-devices
```
Or check the available devices in Python.

```python
import qai_hub as hub

devices = hub.get_devices()
print(devices)
```