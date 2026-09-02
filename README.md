# Vim-RUST

Vim-RUST v0.4.0 is a Windows x64 DMA-based companion tool for Rust.

## Features

- English and Chinese user interface
- Read-only DMA mode
- Player ESP with boxes, names, skeletons, health, and player information
- Filters for sleepers, wounded players, NPCs/wildlife, spectators, and teammates
- Player glow and off-screen FOV arrows
- Item ESP and filtering
- Radar and map-related options
- Aim configuration with KMBox Net / B Pro support, disabled by default
- Built-in DMA diagnostics

## Requirements

- Windows x64
- Compatible FPGA/DMA device using FTDI FT601/D3XX
- FTDI D3XX x64 driver
- USB 3.x connection
- `RustClient.exe` running before launch

## Installation

1. Download `Vim-RUST-v0.4.0-x64.zip` from the GitHub Releases page.
2. Extract the entire archive.
3. Keep `RustDMA.exe`, `Run-RustDMA.cmd`, `runtime`, and `assets` together in the extracted release directory.
4. Connect the DMA device and confirm that the FTDI D3XX x64 driver is installed.
5. Start Rust and wait for `RustClient.exe` to become available.
6. Run `Run-RustDMA.cmd`.

## Troubleshooting

- If the device is not found, check the board power, USB 3.x cable/port, and FTDI D3XX x64 driver.
- Exit code `3` means the DMA capture device could not be initialized.
- Exit code `4` means `RustClient.exe` was not found or was not ready for module validation.
- Run `Diagnose-DMA.ps1` and review `dma-diagnostic.txt` for additional information.

## Release asset verification

**File:** `Vim-RUST-v0.4.0-x64.zip`  
**Size:** `15,134,803 bytes (14.43 MiB)`

**SHA-256:**

```text
B7043A35C3E9275A66640959B8E79DFD434728812274E32B628012B398CF0D7F
```

Verify on Windows PowerShell:

```powershell
Get-FileHash .\Vim-RUST-v0.4.0-x64.zip -Algorithm SHA256
```

## Distribution notice

This repository provides a packaged binary release and its documentation. The package is provided as-is, without warranty. No claim is made that it is undetected or anti-cheat safe.

Source code and an open-source license are not included in this repository.
