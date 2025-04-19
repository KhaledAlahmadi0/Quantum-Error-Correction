# 🧬 Shor Code Implementation in Qiskit

This project demonstrates the implementation of **Shor’s Code**, a foundational quantum error correction code, using IBM’s Qiskit framework.

## 📘 Overview

Shor's Code encodes a single logical qubit into 9 physical qubits to protect against arbitrary single-qubit errors (bit-flip, phase-flip, or both).

---

## 🚀 What’s Inside

- 🧱 9-qubit encoding of a logical qubit
- ❌ Injection of simulated quantum errors
- 🧠 Syndrome measurement for error detection
- 🔧 Recovery operations for correction
- 📉 Final measurement and verification

---

## 📁 Files

- `shor_code_qiskit.ipynb`: Main Jupyter Notebook implementing Shor’s Code
- `README.md`: This documentation

---

## 📦 Requirements

Install Qiskit and required tools:

```bash
pip install qiskit qiskit-aer matplotlib
```

---

## ▶️ How to Run

1. Open the notebook `shor_code_qiskit.ipynb` in Jupyter.
2. Run the cells sequentially.
3. View the final state and histograms to confirm successful correction.

---

## 📚 References

- [Qiskit Textbook: Quantum Error Correction](https://qiskit.org/textbook/ch-error-correction/index.html)
- [Wikipedia: Shor's Code](https://en.wikipedia.org/wiki/Shor_code)

---

## 🧠 Notes

- Shor’s Code demonstrates protection against arbitrary single-qubit noise using **concatenation of 3-qubit bit-flip and phase-flip codes**.
- This implementation is educational and simulates errors and corrections using classical control in Qiskit.

---

