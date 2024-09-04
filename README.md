# Mosaico Docs

Welcome to the Mosaico Documentation!

This repository contains the documentation for the Mosaico ecosystem, available at [mosaico.murkrowdev.org/docs](https://mosaico.murkrowdev.org/docs).

---

## Table of Contents

1. [Introduction](#introduction)
2. [Requirements](#requirements)
3. [Installation](#installation)
---

## Introduction
Mosaico allows users and developers to create, share, and display custom widgets on an LED matrix.
More infos about the project can be found on the [Mosaico Website](https://mosaico.murkrowdev.org).

---

## Requirements
- Python
- Pip
---

## Building the Documentation

```bash
git clone --depth 1 https://github.com/mosaico-matrix/mosaico-docs
cd mosaico-docs

# Create venv and install dependencies
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Build the docs
mkdocs build
```

---

## Contributing

We welcome contributions! Feel free to open an issue or submit a pull request.

---

## License

This software is licensed under the AGPL-3.0 License. A copy of the license can be found in the [LICENSE](./LICENSE) file.

---

Feel free to reach out if you have any questions or need further assistance!