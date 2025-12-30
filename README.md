# specRL - Speculative Decoding RL

The C++ modules for specRL (Suffix Tree-based Distributed Draft Worker).

## Overview

This package provides two main modules:

- **cache_updater**: For updating the rollout cache via gRPC communication
- **suffix_cache**: For suffix tree based cache management and speculative decoding

Both modules are implemented in C++ with Python bindings via pybind11.

## Requirements

### System Dependencies

- CMake >= 3.14
- C++17 compatible compiler (GCC 7+, Clang 5+)
- Boost (system, thread)
- gRPC and Protocol Buffers
- xxHash

### Python Dependencies

- Python >= 3.8
- pybind11 >= 2.10.0

## Installation

### Quick Install

Before installing, ensure you have the required system packages:

**Ubuntu/Debian:**
```bash
sudo apt install -y libprotobuf-dev protobuf-compiler libprotoc-dev \
    libgrpc-dev libgrpc++-dev protobuf-compiler-grpc \
    libxxhash-dev libboost-all-dev cmake pkg-config
```

```bash
pip install git+https://github.com/He-Jingkai/specRL.git --no-build-isolation -v
```

**Note:** First-time installation compiles C++ code and may take 5-10 minutes. 

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Acknowledgments

This project leverages the suffix tree implementation from Snowflake's [ArcticInference](https://github.com/snowflakedb/ArcticInference) as its code base.
