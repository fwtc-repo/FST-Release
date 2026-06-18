# FST Open Source Source and Relinking Information

This FST Windows package is intended to keep Qt runtime libraries dynamically linked and replaceable.

## Qt LGPL Relinking Notes

When FST is distributed using open-source Qt under the GNU LGPL v3:

- Qt DLLs are shipped as separate dynamic libraries.
- Users may replace those Qt DLLs with compatible modified Qt builds.
- FST must not prohibit reverse engineering solely for debugging modifications to the LGPL-covered Qt libraries.
- FST does not intentionally modify Qt source code. If this changes, the modified Qt source code must be made available under the applicable Qt open-source license.
- The corresponding Qt source code can be obtained from the Qt source archives for the exact Qt versions used by this release:
  - Qt 6.8.3
  - Qt 5.12.12

## Component Source Locations

The release contains license texts and component notices in `THIRD_PARTY_LICENSES`.

- Qt source archives and license information: https://www.qt.io/download-open-source and https://doc.qt.io
- QWindowKit source: https://github.com/stdware/qwindowkit
- OpenSSL source and license information: https://www.openssl-library.org/source/license/
- ESP Serial Flasher source: https://github.com/espressif/esp-serial-flasher
- CPython source and license information: https://www.python.org/downloads/source/
- stcgal source: https://github.com/grigorig/stcgal
- pyserial source: https://github.com/pyserial/pyserial

## Commercial Qt Builds

If FST is built and distributed under a separate Qt commercial license, follow the commercial license agreement and keep the commercial license records outside the public release package as required by that agreement. The release script's open-source compliance files may still be included as third-party notices for non-Qt components.
