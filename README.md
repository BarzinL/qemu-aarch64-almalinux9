# QEMU for AArch64 on AlmaLinux 9

This repository contains a pre-built version of QEMU 9.1.1 for emulating AArch64 (ARM64) architecture on AlmaLinux 9. This binary has been compiled and tested in an AlmaLinux 9 (x86_64) environment using WSL.

## Features

- Support for AArch64 architecture (ARM64).
- Built on AlmaLinux 9 x86_64 with upstream support.
- Includes additional dependencies such as TPM support, SELinux support, and more.

## Installation

To use the provided `qemu-system-aarch64` binary on your system, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/BarzinL/qemu-aarch64-almalinux9.git
   cd qemu-aarch64-almalinux9
   ```

2. Extract the compressed binary:

  ```bash
  tar -xvJf qemu-system-aarch64.tar.xz
  ```

3. Make the binary executable:

  ```bash
  chmod +x qemu-system-aarch64
  ```

4. Move the binary to a directory in your `$PATH` (e.g., `/usr/local/bin`):

  ```bash
  sudo mv qemu-system-aarch64 /usr/local/bin/
  ```

5. Test that the binary is working by checking its version:

   ```bash
   qemu-system-aarch64 --version
   ```

## Usage

To emulate an AArch64 system with QEMU, you can use the following command as an example:

```bash
qemu-system-aarch64 -M virt -cpu cortex-a57 -m 2048 -nographic -kernel <path-to-kernel> -append "console=ttyAMA0"
```

For more advanced usage, refer to the official [QEMU documentation](https://www.qemu.org/documentation/).

## Compatibility

- Tested with AlmaLinux 9 on x86_64.
- Compatible with ARM64 (AArch64) emulation.

## Contribution

Contributions are welcome! If you find any issues or would like to add features, feel free to open an issue or submit a pull request.

## License

This project is licensed under the GPLv2 License - see the LICENSE file for details.
