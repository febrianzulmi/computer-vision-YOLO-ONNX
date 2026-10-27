# yolov5-onnx

Project detection object YOLOv5 with ONNX Runtime.

##Troubleshoot DLL Error Windows

If you getting error:
```
ImportError: DLL load failed while importing onnxruntime_pybind11_state
```

### Solutiom:

1. **Install Visual C++ Redistributables** (Important!)
   - Download dan install dari: https://aka.ms/vs/17/release/vc_redist.x64.exe
   - Atau cari "Visual C++ Redistributables" di Microsoft Store
   - Restart komputer setelah install

2. **Reinstall onnxruntime**
   ```bash
   uv pip install --force-reinstall onnxruntime
   ```

3. **Alternate: use onnxruntime-directml**
   ```bash
   uv pip uninstall onnxruntime
   uv pip install onnxruntime-directml
   ```

4. **Make surw Python 64-bit**
   - run: `python -c "import platform; print(platform.architecture())"`
   - make sure `64bit`, not `32bit`

## Instalation

```bash
uv sync
```

## Running

```bash
uv run main_video.py
```
