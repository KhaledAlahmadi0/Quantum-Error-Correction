# 🧬 Steane Code Implementation in Qiskit

This project demonstrates a full implementation of the **Steane Code** using IBM’s Qiskit. The Steane Code is a 7-qubit quantum error correction code capable of detecting and correcting any single-qubit error (bit-flip, phase-flip, or both).

---

## 📘 Overview

The Steane Code is a member of the Calderbank–Shor–Steane (CSS) family of quantum error correction codes. It encodes one logical qubit into 7 physical qubits.

---

## 🚀 Features

- 🧱 Encoding a logical qubit into 7 physical qubits
- ❌ Simulating single-qubit errors
- 🧠 Measuring stabilizers (syndromes)
- 🔧 Performing error correction
- 📈 Final measurement and fidelity analysis

---

## 📁 Files

- `steane_code_full_qasm.ipynb`: Jupyter Notebook implementing the full Steane Code
- `README.md`: This documentation file

---

## 📦 Requirements

Make sure you have the following packages installed:

```bash
pip install qiskit qiskit-aer matplotlib
```

---

## ▶️ How to Run

1. Open the notebook `steane_code_full_qasm.ipynb` in Jupyter or VS Code.
2. Run each cell in sequence to:
   - Encode the logical qubit
   - Simulate errors
   - Extract syndrome
   - Apply correction
   - Measure the final state

---

## 🧠 Notes

- The Steane code protects against **any single-qubit Pauli error**.
- It is based on classical [Hamming [7,4,3]] error correcting codes with CSS construction.
- This implementation is a **simulation** and is best used for educational or research purposes.

---

## 📚 References

- [Qiskit Textbook - Steane Code](https://qiskit.org/textbook/ch-error-correction/steane-code.html)
- [Wikipedia: Steane Code](https://en.wikipedia.org/wiki/Steane_code)

---
