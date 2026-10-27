# yolov5-onnx

Project detection object YOLOv5 with ONNX Runtime.

##Troubleshoot DLL Error Windows

Jika Anda mengalami error:
```
ImportError: DLL load failed while importing onnxruntime_pybind11_state
```

### Solutiom:

1. **Install Visual C++ Redistributables** (Paling Penting!)
   - Download dan install dari: https://aka.ms/vs/17/release/vc_redist.x64.exe
   - Atau cari "Visual C++ Redistributables" di Microsoft Store
   - Restart komputer setelah install

2. **Install ulang onnxruntime**
   ```bash
   uv pip install --force-reinstall onnxruntime
   ```

3. **Alternatif: Gunakan onnxruntime-directml**
   ```bash
   uv pip uninstall onnxruntime
   uv pip install onnxruntime-directml
   ```

4. **Pastikan Python 64-bit**
   - Jalankan: `python -c "import platform; print(platform.architecture())"`
   - Harus menunjukkan `64bit`, bukan `32bit`

## Instalasi

```bash
uv sync
```

## Menjalankan

```bash
uv run main_video.py
```
