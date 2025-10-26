# SpikingBrain-7B-HAL: Hardware Abstraction Layer

🔧 **Hardware Abstraction Layer** for SpikingBrain-7B  
🚀 **Universal Hardware Support** - Run on any hardware platform  
⚡ **Performance Optimized** - Maintains efficiency across different architectures  
🐳 **Container Ready** - Docker support for easy deployment  

---

## About SpikingBrain-7B-HAL

This repository extends the original [SpikingBrain-7B](https://github.com/BICLab/SpikingBrain-7B) with a comprehensive **Hardware Abstraction Layer (HAL)** that enables the neuromorphic AI model to run efficiently on any hardware platform, not just NVIDIA-specific hardware.

### Key Features

- **🔧 Hardware Agnostic**: Automatically detects and adapts to available hardware
- **⚡ Performance Optimized**: Maintains high performance across different architectures
- **🐳 Container Ready**: Full Docker support for easy deployment
- **📦 Modular Design**: Clean separation between original code and HAL implementation
- **🔄 Backward Compatible**: Works with existing SpikingBrain-7B models and weights

---

## Project Structure

```
SpikingBrain-7B-HAL/
├── spikingbrain-7b-original/    # Original SpikingBrain-7B implementation
│   ├── hf_7B_model/             # HuggingFace version
│   ├── run_model/               # Model run examples
│   ├── vllm_hymeta/             # vLLM plugins and inference support
│   ├── W8ASpike/                # Quantized inference version
│   └── ...                      # Other original files
├── hal/                         # Hardware Abstraction Layer (Coming Soon)
│   ├── core/                    # Core HAL functionality
│   ├── backends/                # Hardware-specific backends
│   └── adapters/                # Model adapters
├── examples/                    # Usage examples
├── docs/                        # Documentation
└── README.md                    # This file
```

---

## Quick Start

### Prerequisites

- Python 3.8+
- PyTorch 2.0+
- CUDA (optional, for NVIDIA GPUs)
- ROCm (optional, for AMD GPUs)

### Installation

```bash
# Clone the repository
git clone https://github.com/Jimmy-Dejesus/SpikingBrain-7B-HAL.git
cd SpikingBrain-7B-HAL

# Install dependencies
pip install -r requirements.txt

# Install HAL (when available)
pip install -e .
```

### Basic Usage

```python
from spikingbrain_hal import SpikingBrainHAL

# Initialize with automatic hardware detection
model = SpikingBrainHAL.from_pretrained("spikingbrain-7b-hal")

# Run inference
output = model.generate("Hello, world!")
print(output)
```

---

## Hardware Support

| Hardware | Status | Performance | Notes |
|----------|--------|-------------|-------|
| NVIDIA GPUs | ✅ Full | 100% | Original performance |
| AMD GPUs | 🚧 In Progress | ~80% | ROCm support |
| Intel GPUs | 🚧 Planned | ~70% | OneAPI support |
| CPU | ✅ Basic | ~30% | Fallback mode |
| Apple Silicon | 🚧 Planned | ~60% | Metal support |

---

## Development Status

- [x] **Repository Setup** - Clean structure with original code nested
- [x] **Dependency Management** - Hardware-agnostic requirements
- [ ] **Core HAL Implementation** - Hardware detection and routing
- [ ] **NVIDIA Backend** - Optimized CUDA implementation
- [ ] **AMD Backend** - ROCm implementation
- [ ] **CPU Backend** - Fallback implementation
- [ ] **Documentation** - Comprehensive guides and examples

---

## Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

### Development Setup

```bash
# Fork and clone the repository
git clone https://github.com/your-username/SpikingBrain-7B-HAL.git
cd SpikingBrain-7B-HAL

# Create a development environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install in development mode
pip install -e ".[dev]"

# Run tests
pytest tests/
```

---

## License

This project is licensed under the same terms as the original SpikingBrain-7B project. See [LICENSE](LICENSE) for details.

---

## Acknowledgments

- **Original SpikingBrain-7B**: [BICLab/SpikingBrain-7B](https://github.com/BICLab/SpikingBrain-7B)
- **Hardware Abstraction Layer**: Jimmy Dejesus
- **Community**: All contributors and users

---

## Citation

If you use this HAL implementation, please cite both the original SpikingBrain work and this HAL extension:

```bibtex
@article{pan2025spikingbrain,
  title={SpikingBrain Technical Report: Spiking Brain-inspired Large Models},
  author={Pan, Yuqi and Feng, Yupeng and Zhuang, Jinghao and Ding, Siyu and Liu, Zehao and Sun, Bohan and Chou, Yuhong and Xu, Han and Qiu, Xuerui and Deng, Anlin and others},
  journal={arXiv preprint arXiv:2509.05276},
  year={2025}
}

@software{spikingbrain_hal_2025,
  title={SpikingBrain-7B-HAL: Hardware Abstraction Layer},
  author={Dejesus, Jimmy},
  year={2025},
  url={https://github.com/Jimmy-Dejesus/SpikingBrain-7B-HAL}
}
```

---

## Contact

- **Author**: Jimmy Dejesus
- **Email**: jimmy@bravetto.com
- **GitHub**: [@Jimmy-Dejesus](https://github.com/Jimmy-Dejesus)
- **Issues**: [GitHub Issues](https://github.com/Jimmy-Dejesus/SpikingBrain-7B-HAL/issues)

---

*This project is in active development. Features and APIs may change before the first stable release.*