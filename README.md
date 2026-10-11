# SerialPortManager

A Windows application for working with serial ports. It is proprietary software, licensed and not sold: you can
evaluate it without a license file, and a license file unlocks the licensed features. Read
[LICENSE.md](LICENSE.md) before use.

| | |
|---|---|
| **Version** | 0.3.0-rc.6 (release candidate) |
| **Platform** | Windows, 64-bit (`x64`) and 32-bit (`Win32`) |
| **Licensing** | Evaluation without a license file; full features with a signed `license.lic` |
| **Source code** | Private (this repository contains the program only) |
| **Manuals** | Manual and Quick Guide, English and Italian (`manuals/` next to the program) |

## Which folder do I use?

Each folder is a complete, self-contained copy of the program. Use **one** of them.

| Folder | Build | What it contains |
|---|---|---|
| `x64/Release/` | b106 | One standalone `SerialPortManager.exe`, 64-bit |
| `x64/Release_DLL/` | b108 | A smaller 64-bit `SerialPortManager.exe` plus its DLLs |
| `Win32/Release/` | b107 | One standalone `SerialPortManager.exe`, 32-bit |
| `Win32/Release_DLL/` | b109 | A smaller 32-bit `SerialPortManager.exe` plus its DLLs |

Use `x64` on 64-bit Windows; use `Win32` only if you need the 32-bit version. Keep everything in the folder
together: the `.exe`, the `SerialPortManager data` folder, the `manuals` folder and, in the `_DLL` folders, the
`.dll` files.

To get the files, use **Code > Download ZIP** on this page, or clone the repository.

## Verify your download

The program is not code-signed, so Windows SmartScreen may show a warning the first time you run it. Before
running, check that the file matches the published checksum in `SHA256SUMS.txt`.

PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 ".\x64\Release\SerialPortManager.exe"
```

Compare the result with the line for that file in `SHA256SUMS.txt`. On Linux or macOS use
`sha256sum -c SHA256SUMS.txt` from the repository folder.

## Licensing

- **Evaluation:** without a license file the program can be used on one computer to evaluate it. The evaluation
  period is stated by the program itself.
- **License file:** a digitally signed `license.lic`, issued by the author, states the licensee, the licensed
  features (edition), the licensed computers, the term and the covered versions. Licensing enquiries, license
  requests and renewals: please open an issue in this repository.
- **Please do not redistribute** the program or a license file; get it from this repository. The full terms are in
  [LICENSE.md](LICENSE.md).

## Safety

The program communicates with external equipment. You are responsible for checking that it suits your purpose
and for the safe operation of any equipment connected to it.

## Third-party components

The program includes or links wxWidgets, SQLite, the serial library (MIT) and TweetNaCl (public domain). Each is
used under its own license, listed in [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

## Support

Questions and problem reports: please open an issue in this repository.

Copyright (C) 2026 Fation Coga. All rights reserved.
