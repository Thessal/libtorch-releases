# libtorch-releases

This repository exists to host Linux Arm64 (aarch64) libtorch builds. The official PyTorch release pipeline currently publishes libtorch archives for x86_64 (amd64) only, so we provide a place for the community to download Arm64-compatible binaries.

## Availability
- Target: Linux Arm64 (no macOS/Apple Silicon support yet).
- Current version: `v2.4.0`. Each repository tag corresponds to the upstream PyTorch release used for the build.
- Release assets: `libtorch-aarch64.tar.gz` is attached to the GitHub release for the matching tag and is not tracked in the source tree.

## Downloading
1. Choose the release tag that matches the PyTorch version you need (currently `v2.4.0`).
2. Download the attached `libtorch-aarch64.tar.gz` from that release page.
3. Extract with `tar -xzf libtorch-aarch64.tar.gz` and configure your build system to use the extracted directory.

## Contributing new builds
- Match the upstream PyTorch version and configuration (ABI, CUDA settings, dependencies).
- Package the archive as `libtorch-aarch64.tar.gz`.
- Attach the archive when creating the release for the corresponding tag, and clearly note the PyTorch commit/version used.

If upstream PyTorch starts shipping Linux Arm64 libtorch archives, we can retire this repository.

## Useful links 
- Pytorch versions : https://pytorch.org/get-started/previous-versions/
- ubuntu version : lsb_release -a
- cuda version : nvidia-smi
- cuda_arch : https://developer.nvidia.com/cuda/gpus
