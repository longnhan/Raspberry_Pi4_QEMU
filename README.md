# Raspberry Pi Camera QEMU Environment

This project provides a **QEMU-based virtual environment** for developing and testing Raspberry Pi camera applications. It enables running Raspberry Pi OS, testing kernel modules, and simulating camera behavior without real hardware.

## Features

- Emulates **Raspberry Pi 4** in QEMU
- Supports **Raspberry Pi OS (Debian 11-based)**
- Includes scripts for **automated setup and kernel compilation**
- Allows **camera development and testing** in a virtual environment

## Requirements

Ensure you have the following installed:

- QEMU (`qemu-system-aarch64`)
- Git LFS (`git lfs install`)
- Required dependencies (install with `sudo apt install qemu-utils libguestfs-tools`)

## Setup

1. Clone the repository:

   ```bash
   git clone --recursive https://github.com/longnhan/Raspberry_Pi4_QEMU.git
   cd Raspberry_Pi4_QEMU
   ```

2. Install Git LFS:

   ```bash
   git lfs install
   git lfs pull
   ```

3. Extract the `qemu2.7z` archive:

   ```bash
   7z x qemu2.7z
   ```

## Running QEMU

Start the emulated Raspberry Pi:

```bash
./qemu2/qemu_run.sh
```

This will launch Raspberry Pi OS inside QEMU.

### Default Credentials

- **Username:** `pi`
- **Password:** `1`

### SSH Access

To connect via SSH, use:

```bash
ssh -p 2222 pi@127.0.0.1
```

## Troubleshooting

- **Large file errors in Git LFS?**\
  Run:
  ```bash
  git lfs ls-files
  git lfs push --all origin
  ```
- **QEMU boot issues?**\
  Ensure the `.img` file is correctly built and accessible.

## Contributing

Feel free to open **issues** or submit **pull requests** to improve the project.

## License

This project is licensed under the **MIT License**.

