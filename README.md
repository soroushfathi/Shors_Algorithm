# Shors_Algorithm
Shor's ALgorithm implemented factorizing 63 on Qiskit, Python 3.X

Shor's algorithm performs integer factorization on a quantum computer, which can break many asymmetric (public/private key) cryptosystems, such as RSA or Diffie–Hellman. Many secure protocols, including HTTPS, SSH, and TLS, rely on these cryptosystems to guarantee encryption and authenticity. In mathematical terms, Shor's solves the hidden subgroup problem for finite Abelian groups. In layman's terms, Shor's algorithm could expose encrypted information. This implementation simulates a quantum circuit using state vectors and unitary mappings.

Where:
PERIODS is the number of successful circuit rounds to run before finding the GCD of their results
ATTEMPTS is the number of attempted circuit simulations to run per round
NEIGHBORHOOD is the range of values to check near the circuit output register, given as a percentage of N
N is the composite, positive integer to factor

Refrences: 
  - https://en.wikipedia.org/wiki/Shor%27s_algorithm
  - Chapter 6.5: Shor's Factorizing Algorithm, Yanofsky_2008
  - Qiskit: https://qiskit.org/textbook/ch-algorithms/shor.html
