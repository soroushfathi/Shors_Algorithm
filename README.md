# Shors_Algorithm
It is a quantum computer algorithm which its used for finding the prime factor of an integer. It was developed in 1994 by the American mathematician Peter Shor. In the quantum computer to factor an integer N, Shor’s algorithm will run in polynomial time which means the time taken polynomial in log N. Where N is an integer, and its size is given as an input. The efficiency of the Shor’s algorithm is due to the efficiency of the QFT and the modular exponentiation. 

Shor's ALgorithm implemented factorizing 63 on Qiskit using SWAP gates, Python 3.X

# Motivation
at Qiskit, it shows that we can acheive factroizing the number 15 by only using SWAP Gates, however we wanted achieve writing the full algorithm using SWAP gates only and factorizing the number 63. 

If there is a quantum computer with a sufficient number of qubits that can operate without succumbing to the quantum noise and other quantum decoherence phenomena, then here Shor’s algorithm can be used to break the public key cryptography schemes such as the RSA. 

## How Does Shor’s Algorithm Work? 
Since its a hybrid algorithm which is means it has two parts the classical and the quantum parts and works as the following: 
The classical part: 
  1) Pick a random number (𝑎) where 1 < 𝑎 < 𝑁.
  2) Compute  K=𝐺𝐶𝐷(𝑎,𝑁) which is the greatest common factor divisor of a and 𝑁, by using the Euclidean algorithm. 
  3) If K ≠1, then K is a nontrivial factor of N. - break -
  4) Otherwise, use the quantum period finding to find r which is the period of the following function: 𝑓(𝑥)= 𝑎^𝑥 𝑚𝑜𝑑 𝑁. Where r is the smallest      positive integer that satisfies 𝑎^𝑟 = 1 mod N. 
  5) If r is odd, back to step 1. 
  6) If 𝑎𝑟/2 = −1 mod N, back to step 1. 
  7) Otherwise, both 𝐺𝐶𝐷 (𝑎𝑟2/+ 1, 𝑁)  or 𝐺𝐶𝐷 (𝑎𝑟2/− 1, 𝑁) are nontrivial factors of N. 

The quantum part: (period finding) 
If there is a quantum computer with a sufficient number of qubits that can operate without succumbing to the quantum noise and other quantum decoherence phenomena, then Shor’s algorithm can be implemented and used to break public key cryptography schemes such as the RSA.  

The used of the QFT is to transform the states from Fourier basis to computational basis. The Fourier basis is results from applying the c-U gates. Where The period is "encoded" as phases, IQFT helps in restoring the period as 0 and 1 states. 
 
How does it work?  
1) We need to find the coprime number (𝑎) by finding the 𝐺𝐶𝐷(𝑎,63)=1
2) We need to apply for every coprime number (𝑎) this following equation [ 𝑎∗𝑦 𝑚𝑜𝑑 63], where 𝑦 is a random number form 
1 to 63
3) We will use this special case when we find some numbers sharing the same behavior and they have the same swap circuit but for every odd number we will need to implement an X- gate.

The similarities between all co-primes of 63 are in the attached excel file. However, the following is a simple outline of the SWAP gates drawn for 63 co-primes. 
 
# Requirements
Python 3.x, numpy, matplotlib, qiskit-terra, qiskit-aer, qiskit-aqua


# Refrences: 
  - https://en.wikipedia.org/wiki/Shor%27s_algorithm
  - Chapter 6.5: Shor's Factorizing Algorithm, Yanofsky_2008
  - IBM Quantum Experience
  - Qiskit: https://qiskit.org/textbook/ch-algorithms/shor.html
