# Shors_Algorithm
Shor's ALgorithm implemented factorizing 63 on Qiskit, Python 3.X

Shor's algorithm performs integer factorization on a quantum computer, which can break many asymmetric (public/private key) cryptosystems, such as RSA or Diffie–Hellman. Many secure protocols, including HTTPS, SSH, and TLS, rely on these cryptosystems to guarantee encryption and authenticity. In mathematical terms, Shor's solves the hidden subgroup problem for finite Abelian groups. In layman's terms, Shor's algorithm could expose encrypted information. This implementation simulates a quantum circuit using state vectors and unitary mappings.

Where:
- PERIODS is the number of successful circuit rounds to run before finding the GCD of their results

#Requirements
Python 3.x, numpy, matplotlib, qiskit-terra, qiskit-aer, qiskit-aqua


Refrences: 
  - https://en.wikipedia.org/wiki/Shor%27s_algorithm
  - Chapter 6.5: Shor's Factorizing Algorithm, Yanofsky_2008
  - IBM Quantum Experience
  - Qiskit: https://qiskit.org/textbook/ch-algorithms/shor.html
