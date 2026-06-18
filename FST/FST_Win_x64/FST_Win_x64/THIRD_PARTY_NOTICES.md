# FST Third-Party Notices

This file lists the third-party software components that are shipped with, linked into, or otherwise redistributed as part of the FST Windows release package.

This document is an engineering compliance notice, not a replacement for the original license texts. The full license texts are shipped in the `THIRD_PARTY_LICENSES` directory next to this file.

## Qt

- Components: Qt 6.8.3 runtime libraries used by `FST.exe`, `updata_copy.exe`, and `fst_bluetooth_proxy.exe`; Qt 5.12.12 runtime libraries used by `win32_proxy.exe`.
- Current runtime form: dynamically linked DLLs.
- Expected Qt modules in the FST release: Qt Core, Qt Widgets, Qt Gui, Qt Network, Qt SerialPort, Qt Bluetooth, Qt Core5Compat, and Qt 5 Core/Network for `win32_proxy.exe`.
- License basis for open-source Qt usage: GNU LGPL v3 or, for separately licensed builds, the applicable Qt commercial license.
- FST does not intentionally ship Qt GPL-only modules. The release script blocks known GPL-only Qt runtime DLLs unless explicitly overridden for a separately licensed build.
- Source and replacement information: see `OPEN_SOURCE_SOURCE_OFFER.md`.

## QWindowKit

- Component: QWindowKit 1.5.1.0
- Use in FST: frameless/window chrome support, linked into the application build.
- License: Apache License 2.0
- License file: `THIRD_PARTY_LICENSES/QWindowKit-Apache-2.0.txt`

## QWindowKit helper projects

- Component: QWindowKit `qmsetup`
- License: MIT
- License file: `THIRD_PARTY_LICENSES/QWindowKit-qmsetup-MIT.txt`

- Component: QWindowKit `syscmdline`
- License: MIT
- License file: `THIRD_PARTY_LICENSES/QWindowKit-syscmdline-MIT.txt`

## OpenSSL

- Component: OpenSSL 3.5.4 static libraries
- Use in FST: cryptographic support in the license module.
- License: Apache License 2.0
- License file: `THIRD_PARTY_LICENSES/OpenSSL-Apache-2.0.txt`
- Version file: `THIRD_PARTY_LICENSES/OpenSSL-version.txt`

## Espressif ESP Serial Flasher

- Component: `espressif/esp-serial-flasher` 1.11.0 source snapshot
- Use in FST: native ESP32 flashing backend compiled into FST.
- Pinned commit: `f1cccac82a41f6d494d953359d5ca2f5d70a9b12`
- License: Apache License 2.0
- License file: `THIRD_PARTY_LICENSES/esp-serial-flasher-Apache-2.0.txt`
- Notice file: `THIRD_PARTY_LICENSES/ESP_SERIAL_FLASHER_NOTICES.md`

## STC Python Backend

FST redistributes a private Python runtime backend for STC flashing so users do not need to install Python manually.

- Component: CPython Windows embeddable package 3.13.13, 64-bit
- License: Python Software Foundation License
- License file: `THIRD_PARTY_LICENSES/CPython-PSF-License.txt`

- Component: `grigorig/stcgal` 1.10 source snapshot
- Pinned commit: `fdf5fdd60515a260bb303dcf7b251c2b2671f91c`
- License: MIT
- License file: `THIRD_PARTY_LICENSES/stcgal-MIT.txt`

- Component: `pyserial` 3.5
- License: BSD
- License file: `THIRD_PARTY_LICENSES/pyserial-BSD.txt`

- Backend detail notice: `THIRD_PARTY_LICENSES/STC_PYTHON_BACKEND_NOTICES.md`

## MinGW/GCC Runtime Libraries

The Windows release may include runtime DLLs from the MinGW/GCC toolchains used to build the Qt applications, including files such as `libgcc_s_*.dll`, `libstdc++-6.dll`, and `libwinpthread-1.dll`.

- Component family: GCC runtime libraries and MinGW-w64 runtime libraries
- Typical licenses: GPL with GCC Runtime Library Exception, LGPL, permissive MinGW-w64 runtime terms, public domain notices, and related notices depending on the individual runtime file.
- License files:
  - `THIRD_PARTY_LICENSES/GCC-GPL-3.0.txt`
  - `THIRD_PARTY_LICENSES/GCC-Runtime-Library-Exception.txt`
  - `THIRD_PARTY_LICENSES/MinGW-w64-runtime.txt`
  - `THIRD_PARTY_LICENSES/MinGW-w64.txt`
  - `THIRD_PARTY_LICENSES/winpthreads.txt`

## Microsoft Visual C++ Runtime Libraries

The Windows release may include Microsoft Visual C++ runtime DLLs required by the MSVC-built Bluetooth proxy, such as `vcruntime*.dll`, `msvcp*.dll`, and `concrt*.dll`.

- Component family: Microsoft Visual C++ Redistributable runtime libraries
- Use in FST: runtime support for `bluetooth_proxy/fst_bluetooth_proxy.exe`
