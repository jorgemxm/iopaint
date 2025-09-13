# io-Paint
Image inpainting tool powered by SOTA AI Model. Remove any unwanted object, defect, people from your pictures or erase and replace(powered by stable diffusion) any thing on your pictures.
- https://github.com/Sanster/IOPaint
- https://www.iopaint.com/

## Torchvision
- https://pytorch.org/get-started/locally/

## Install
```sh
mkdir iopaint-app
uv init --bare -p 3.11
uv venv -p 3.11
uv add iopaint

#--- MacOS ---
# No extra steps

#--- Linux ---
uv pip uninstall torch torchvision
uv pip install torch==2.8.0 torchvision==0.23.0 --index-url https://download.pytorch.org/whl/rocm6.4
# Test ROCm
python -c "import torch; print(f'PyTorch version: {torch.__version__}'); print(f'Cuda available: {torch.cuda.is_available()}'); print(f'Device name: {torch.cuda.get_device_name(0) if torch.cuda.is_available() else None}')"

```

## Run with Model
- https://www.iopaint.com/models
- Recommended models: `mat`, `lama`, `migan` (minimal size)
- In Painting: `zits`
- High Resolution: `ldm`
```sh
iopaint start --model zits --port=8888
iopaint start --model mat --port=8888

iopaint start --model=lama --device=cpu --port=8080
```


