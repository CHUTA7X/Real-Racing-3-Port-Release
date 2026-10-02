[README(1).md](https://github.com/user-attachments/files/32985014/README.1.md)
# Real-Racing-3-Port-Release
New Real Racing 3 port for PS vita Based on 1.4.0 MALI graphics version. 
# Real Racing 3 - PlayStation Vita Port

Native port loader for *Real Racing 3* (v1.4.0 ROW Mali ETC1 edition) targeting the PlayStation Vita using [vitaGL](https://github.com/Rinnegatamante/vitaGL), [vitashark](https://github.com/Rinnegatamante/vitashark), and [kubridge](https://github.com/TheOfficialFloW/kubridge).

## Features & Implementation Highlights
- **Direct GLES 2.0 Mapping**: Custom bridge to vitaGL with shader translation via vitashark/shaccCg.
- **Hardware-accelerated Textures**: ETC1 decompression on CPU with hardware mipmap downscaling on PS Vita GPU.
- **Offscreen Framebuffer Management**: Full support for game FBO rendering and post-processing.
- **Input Mapping**: PS Vita buttons and touch mapping.
- **Network Logging**: Live UDP logging support on port 4444.

## Building
Requirements:
- [VitaSDK](https://vitasdk.org/)
- `libvitaGL`, `vitashark`, `mathneon`, `taihen`, `kubridge`

```bash
mkdir -p build && cd build
cmake ..
make -j$(nproc) eboot
```

## Running
Install data to `ux0:data/rr3/` and binary to `ux0:app/RR3VITA01/eboot.bin`.
