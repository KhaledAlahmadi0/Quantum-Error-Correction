# 🧪 Surface Code: Qubit 4 Focused Implementation

This notebook demonstrates a **simplified quantum error correction using surface code**, specifically targeting **Qubit 4**. The goal is to simulate bit-flip error detection (X error), measure stabilizers, and verify the detection logic using ancilla qubits.

## 📋 Overview

This implementation includes:

- ✅ Encoding simplified X and Z stabilizers **around qubit 4**
- ⚠️ Injecting an **X (bit-flip) error** manually on Qubit 4
- 🧠 Measuring stabilizers using ancilla qubits
- 🔧 Manual error correction (optional)
- 📈 Final measurements to verify detection and correction

---

## 🧱 Qubit Roles

| Qubit | Role                        |
|-------|-----------------------------|
| 1, 3, 5 | Neighbors of Qubit 4 (used in stabilizers) |
| 4     | **Target data qubit (corrupted intentionally)** |
| 8     | Ancilla for **Z-stabilizer** (phase flip detection) |
| 9     | Ancilla for **X-stabilizer** (bit flip detection) |

---

## 📌 How It Works

1. **Bit-flip error** is injected on qubit 4:
   ```python
   qc.x(4)
   ```

2. **Stabilizer checks** are applied:
   - X-stabilizer via Hadamard and CNOTs (using qubit 9)
   - Z-stabilizer using CNOTs (using qubit 8)

3. **Syndrome extraction**: 
   ```python
   qc.measure(9, 9)
   qc.measure(8, 8)
   ```

4. (Optional) **Manual correction**:
   ```python
   qc.x(4)
   ```

5. **Final measurement** of data qubits:
   ```python
   qc.measure(range(8), range(8))
   ```

---

## 📊 Sample Output

You will see two histograms:
1. **Syndrome Measurement**: reveals which stabilizers detected an error
2. **Final State Measurement**: shows logical qubit values before correction

---

## ▶️ How to Run

Make sure you have Qiskit and the Aer simulator installed:

```bash
pip install qiskit qiskit-aer matplotlib
```

Run the notebook using Jupyter or any Python environment that supports Qiskit.

---

## 🧠 Notes

- This is a **simplified surface code** and does not include full decoding logic.
- Only one data qubit is intentionally flipped to demonstrate basic stabilizer behavior.
- The correction step is manual to help visualize how the syndrome indicates errors.

---

## 📁 Files

- `surface_code_q4.ipynb` – Main notebook with full implementation
- `README.md` – This documentation

---

## 📚 References

- [Qiskit Textbook: Quantum Error Correction](https://qiskit.org/textbook/ch-error-correction/index.html)
- [Wikipedia: Surface Code](https://en.wikipedia.org/wiki/Surface_code)
