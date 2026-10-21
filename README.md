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
## Licenses / Licencias

This port uses **vitaGL** (modified) and **vitaShaRK** by Rinnegatamante (LGPL-3.0) and **mpg123** (LGPL-2.1). The source code of the modified vitaGL and the package to relink `eboot.bin` with other versions of these libraries are attached to every release as `RR3_v<version>_LGPL.zip`. Third-party notices: [THIRD_PARTY_LICENSES.txt](THIRD_PARTY_LICENSES.txt). The rest of the port is not open source.

Este port usa **vitaGL** (modificada) y **vitaShaRK** de Rinnegatamante (LGPL-3.0) y **mpg123** (LGPL-2.1). El código de la vitaGL modificada y el paquete para reenlazar `eboot.bin` con otras versiones de esas librerías van en cada release como `RR3_v<versión>_LGPL.zip`. Avisos de terceros: [THIRD_PARTY_LICENSES.txt](THIRD_PARTY_LICENSES.txt). El resto del port no es de código abierto.

Real Racing 3 is property of Electronic Arts. No EA files are distributed. / Real Racing 3 es propiedad de Electronic Arts. No se distribuye ningún archivo de EA.
