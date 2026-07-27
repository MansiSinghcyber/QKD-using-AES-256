# QKD-using-AES-256
Quantum Cryptography Key Management Using AES-256: A Classical Simulation Approach with Qiskit and PennyLane
# Quantum Cryptography Key Management Using AES-256
### A Classical Simulation Approach with Qiskit and PennyLane

> A hybrid cryptographic framework that combines **BB84-inspired Quantum Key Distribution (QKD)** with **AES-256 encryption**, simulated entirely on classical hardware using **Qiskit**, **PennyLane**, and **Google Colab**.

---

## 📌 Overview

Quantum computing poses a significant challenge to today's cryptographic systems. Algorithms such as **RSA** and **Elliptic Curve Cryptography (ECC)** become vulnerable once scalable quantum computers become available through **Shor's Algorithm**, while symmetric encryption experiences reduced security due to **Grover's Algorithm**.

This project demonstrates a **hybrid cryptographic architecture** that:

- Simulates the BB84 Quantum Key Distribution protocol
- Generates secure quantum-inspired keys
- Converts generated keys into AES-256 compatible keys using SHA-256
- Encrypts and decrypts messages securely
- Evaluates Quantum Bit Error Rate (QBER)
- Performs entropy and randomness analysis

Unlike physical QKD implementations, this framework requires **no quantum hardware**, making it ideal for education, research, and experimentation. :contentReference[oaicite:1]{index=1}

---

# ✨ Features

- BB84 Quantum Key Distribution Simulation
- AES-256 Encryption & Decryption
- SHA-256 Key Derivation
- QBER (Quantum Bit Error Rate) Analysis
- Sifted Key Generation
- Basis Matching Analysis
- Randomness & Entropy Evaluation
- Noise Simulation
- Alice/Bob Quantum Circuit Visualization
- Google Colab Compatible
- Fully Classical Simulation
- Built using Open Source Quantum Libraries

---

# 📚 Motivation

Traditional public-key cryptography is becoming increasingly vulnerable with the advancement of quantum computing.

This project explores how **quantum-inspired key exchange** can strengthen symmetric encryption without requiring expensive quantum communication hardware.

The work bridges:

- Classical Cryptography
- Quantum Cryptography
- Post-Quantum Security
- Hybrid Cryptographic Architectures

making advanced cryptography accessible to students and researchers. :contentReference[oaicite:2]{index=2}

---

# 🛠 Technologies Used

| Technology | Purpose |
|------------|---------|
| Python | Programming Language |
| Qiskit | Quantum Circuit Simulation |
| PennyLane | Quantum Machine Learning & Circuit Simulation |
| NumPy | Numerical Computation |
| Matplotlib | Graph Generation |
| Google Colab | Development Environment |
| hashlib | SHA-256 Key Derivation |
| PyCryptodome | AES-256 Encryption |

---

# 📂 Project Structure

```
Quantum-Cryptography-AES256/
│
├── README.md
├── requirements.txt
├── main.py
├── bb84.py
├── aes256.py
├── key_generation.py
├── qber.py
├── entropy.py
├── visualization.py
├── results/
│   ├── basis_match.png
│   ├── qber_graph.png
│   ├── entropy_plot.png
│   └── quantum_circuit.png
│
├── paper/
│   └── Quantum_Cryptography_Key_Management.pdf
│
└── LICENSE
```

---

# 🔐 Working Principle

## Step 1 — Alice Generates Random Bits

Alice generates:

- Random binary bits
- Random encoding bases

These represent the information she wishes to transmit securely.

---

## Step 2 — Quantum State Preparation

Using Qiskit:

- Hadamard Gates
- Computational Basis
- Measurement Operations

simulate the BB84 protocol.

---

## Step 3 — Bob Measures the Qubits

Bob independently selects random bases.

After measurement:

- Matching bases are retained.
- Non-matching bases are discarded.

This process creates the **Sifted Key**.

---

## Step 4 — Key Derivation

The sifted key is passed through

```
SHA-256
```

to generate a secure

```
256-bit AES Key
```

---

## Step 5 — AES Encryption

The generated key is used for

- AES-256 Encryption
- AES-256 Decryption

ensuring confidentiality of transmitted messages.

---

## Step 6 — Security Analysis

The framework computes

- Basis Match Frequency
- Entropy
- Randomness
- QBER
- Noise Resilience

to evaluate the security of generated keys. :contentReference[oaicite:3]{index=3}

---

# 🔬 Simulation Workflow

```
Alice
   │
   ▼
Generate Random Bits
   │
   ▼
Choose Random Bases
   │
   ▼
Qiskit Circuit
   │
   ▼
Quantum Transmission
   │
   ▼
Bob Measures
   │
   ▼
Basis Reconciliation
   │
   ▼
Sifted Key
   │
   ▼
SHA-256
   │
   ▼
AES-256 Key
   │
   ▼
Encryption / Decryption
   │
   ▼
Security Evaluation
```

---

# 📊 Experimental Results

The implementation demonstrates:

### ✔ Approximately 50% Basis Match

As expected from the BB84 protocol.

---

### ✔ High Entropy Keys

Generated sifted keys exhibit nearly uniform randomness.

---

### ✔ Low Quantum Bit Error Rate

QBER remains below acceptable thresholds under moderate noise.

---

### ✔ Successful AES Encryption

All encrypted messages are successfully decrypted using quantum-derived keys.

---

### ✔ Noise Analysis

The simulation studies how increasing noise impacts QBER and key usability. :contentReference[oaicite:4]{index=4}

---

# 📈 Performance Metrics

The project evaluates:

- Basis Match Frequency
- Key Entropy
- Quantum Bit Error Rate (QBER)
- Noise Resilience
- AES Encryption Success Rate
- Randomness Distribution

---

# 🧪 Example Output

```
Original Message:
Hello Quantum World

Generated Sifted Key:
1010110010100110...

SHA-256 Key:
7f91d87e...

AES Ciphertext:
A4F219D3...

Recovered Plaintext:
Hello Quantum World

QBER:
4.2%

Basis Match:
51%

Entropy:
0.998
```

---

# 🚀 Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Quantum-Cryptography-AES256.git
```

Move into the project

```bash
cd Quantum-Cryptography-AES256
```

Install dependencies

```bash
pip install -r requirements.txt
```

Run the project

```bash
python main.py
```

---

# 📦 Requirements

```
python>=3.10

qiskit

pennylane

numpy

matplotlib

pycryptodome

hashlib
```

---

# 📖 Research Contributions

This project contributes by providing:

- A lightweight BB84 simulation
- AES-256 integration with quantum-derived keys
- QBER-based security evaluation
- Entropy validation
- An educational framework executable on classical hardware
- A practical bridge between quantum cryptography theory and implementation :contentReference[oaicite:5]{index=5}

---

# ⚠ Limitations

- Does not require real quantum hardware
- Photon loss is not modeled
- Detector attacks are not simulated
- Side-channel attacks are not included
- Multi-user quantum networks are outside the current scope

---

# 🔮 Future Work

Future improvements include:

- Integration with NIST Post-Quantum Cryptography (ML-KEM, Dilithium)
- Deployment on IBM Quantum or AWS Braket
- Physical QKD testbed validation
- Multi-user secure quantum cloud environments
- Performance benchmarking against PQC algorithms
- Educational modules for quantum cryptography training :contentReference[oaicite:6]{index=6}

---

# 📄 License

This project is licensed under the **MIT License**.



**GitHub:** https://github.com/yourusername

**Email:** your-email@example.com
