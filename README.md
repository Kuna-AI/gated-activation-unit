# Gated Activation Unit

The **Gated Activation Unit** is a simple mechanism designed to modulate input values based on a threshold and a gating factor. It selectively scales values below the threshold while leaving values above the threshold unchanged.

---

## Formula

The GAU operation can be described mathematically as:

if x_i < threshold:
    x_i * sigmoid(harshness)
else:
    x_i

Where:
- x_i: The i-th element of the input.
- threshold: A scalar that defines the boundary for gating. (Initialized as 0.5)
- harshness: A scalar factor (typically in [0, 1]) that determines how much the values below the threshold are scaled. (Initialized as 0.5)

**All parameters are typically learnt during training.**

---

## Implementation

You can find framework-specific implementations of the GAU in the `implementations/` folder. Current implementations include:

- **PyTorch:** `implementations/pytorch.py`

Each implementation adheres to the same formula, ensuring consistency across frameworks.

---

## Contributing

Contributions are welcome! To add more framework-specific implementations or improve existing ones, feel free to submit a pull request.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
