# Discrete Mathematics in Cryptography

<p align="center">
  <strong>Exploring the Mathematical Foundations of Modern Cryptography</strong><br>
  Discrete Mathematics • Number Theory • RSA • Diffie–Hellman • Finite Fields • Hashing • Post-Quantum Cryptography
</p>

---

## 📌 Overview

Cryptography is one of the most important applications of mathematics in computer science. It provides mathematical techniques for protecting information from unauthorized access, modification, and misuse.

This project explores how **Discrete Mathematics** is used to construct, understand, and analyze cryptographic systems.

Rather than treating cryptography as a collection of isolated algorithms, the project focuses on the mathematical ideas behind those algorithms and shows how concepts such as modular arithmetic, prime numbers, GCD, modular inverses, Euler's Totient Function, groups, finite fields, Boolean algebra, probability, and computational complexity contribute to modern cryptography.

The project also examines the impact of **quantum computing** and the development of **post-quantum cryptography**.

---

## 🎯 Objectives

- Understand the mathematical foundations of cryptography.
- Study the role of discrete mathematics in secure communication.
- Explore modular arithmetic and congruences.
- Understand prime numbers and number-theoretic concepts used in cryptography.
- Study GCD, the Euclidean Algorithm, and modular inverses.
- Understand the mathematical construction of RSA.
- Explore the basic principle of Diffie–Hellman key exchange.
- Study groups, cyclic groups, and finite fields.
- Understand the role of Boolean algebra in symmetric cryptography.
- Explore hashing, probability, and the birthday paradox.
- Understand computational complexity and cryptographic security.
- Examine how quantum computing affects classical public-key cryptography.
- Introduce post-quantum cryptography.

---

# 🧠 Mathematical Foundations

The project connects the following areas of discrete mathematics with cryptography:

| Mathematical Concept | Cryptographic Connection |
|---|---|
| Modular Arithmetic | RSA, Diffie–Hellman |
| Prime Numbers | RSA |
| GCD | Key generation |
| Euclidean Algorithm | Number-theoretic computation |
| Extended Euclidean Algorithm | Modular inverse |
| Euler's Totient Function | RSA |
| Groups | Algebraic cryptography |
| Cyclic Groups | Diffie–Hellman |
| Finite Fields | Modern cryptographic constructions |
| Boolean Algebra | Symmetric cryptography |
| Probability | Hash collisions |
| Combinatorics | Security analysis |
| Computational Complexity | Security assumptions |

---

# 🔐 RSA — Discrete Mathematics in Action

RSA provides a clear example of how several mathematical concepts work together.

### Key generation

Choose two prime numbers:

\[
p, q
\]

Calculate:

\[
n=pq
\]

and:

\[
\phi(n)=(p-1)(q-1)
\]

Choose a public exponent \(e\) such that:

\[
\gcd(e,\phi(n))=1
\]

Then determine the private exponent \(d\) satisfying:

\[
ed\equiv1\pmod{\phi(n)}
\]

The resulting keys are:

- **Public key:** \((e,n)\)
- **Private key:** \((d,n)\)

### Worked example

For:

\[
p=5,\qquad q=11
\]

we obtain:

\[
n=5\times11=55
\]

\[
\phi(55)=(5-1)(11-1)=40
\]

Choose:

\[
e=3
\]

and:

\[
d=27
\]

because:

\[
3\times27=81\equiv1\pmod{40}
\]

For message:

\[
m=7
\]

encryption gives:

\[
c=m^e\pmod n
\]

\[
c=7^3\pmod{55}=13
\]

This small example demonstrates the interaction between prime numbers, Euler's Totient Function, modular arithmetic, and modular inverses.

---

# 🤝 Diffie–Hellman Key Exchange

Diffie–Hellman demonstrates how two parties can establish shared secret information without directly transmitting the secret itself.

Its mathematical foundation includes:

- Modular exponentiation
- Prime numbers
- Cyclic groups
- Discrete logarithms

A simplified flow is:

\`\`\`
Alice                         Bob
  │                             │
  │──── Public Parameters ──────│
  │                             │
  │──── Public Value A ────────>│
  │                             │
  │<──── Public Value B ─────────│
  │                             │
  │       Shared Secret          │
  │        g^(ab)                │
  │                             │
  └──────── Same Secret ─────────┘
\`\`\`

---

# 🔢 Groups and Finite Fields

Groups provide a mathematical framework for studying operations and their properties.

Topics discussed include:

- Sets and binary operations
- Identity elements
- Inverses
- Associativity
- Groups
- Abelian groups
- Cyclic groups
- Finite fields

Finite fields are particularly important because they provide finite mathematical environments in which cryptographic operations can be performed with well-defined algebraic properties.

---

# 🧩 Boolean Algebra and AES

Boolean algebra deals with logical values and operations such as:

- AND
- OR
- NOT
- XOR

These operations are fundamental to digital systems and also contribute to the construction and analysis of symmetric cryptographic algorithms.

The project discusses the connection between Boolean operations, finite mathematical structures, and modern symmetric cryptography such as AES.

---

# #️⃣ Hashing

A cryptographic hash function maps an input message to a fixed-size digest:

\[
h=H(m)
\]

Important properties include:

- Deterministic output
- Efficient computation
- Preimage resistance
- Resistance to finding collisions

The project also introduces the **birthday paradox** to explain why collisions become relevant when a large number of inputs are mapped into a finite output space.

---

# ⏱️ Computational Complexity

Cryptographic security depends not only on mathematical definitions but also on the computational effort required to exploit them.

A cryptographic problem may be theoretically solvable while still being computationally infeasible at the parameter sizes used in practice.

This creates an important relationship:

\[
\text{Mathematical Problem}
\rightarrow
\text{Computational Difficulty}
\rightarrow
\text{Cryptographic Security}
\]

---

# ⚛️ Quantum Computing and the Future

Classical public-key cryptography relies on mathematical problems that are considered difficult for classical computers.

Shor's algorithm provides a quantum approach to integer factorization and discrete logarithms. A sufficiently powerful quantum computer could therefore threaten systems such as RSA and traditional discrete-logarithm-based cryptography.

This motivates **Post-Quantum Cryptography (PQC)**, which investigates cryptographic constructions based on mathematical problems intended to resist both classical and quantum attacks.

The project therefore illustrates an important principle:

> Cryptographic security depends on mathematical assumptions together with the computational model available to an attacker.

---

# 🌍 Real-World Applications

The mathematical principles discussed in this project are relevant to:

- Secure web communication
- Online banking
- Digital payments
- Authentication systems
- Digital signatures
- Cloud security
- Mobile communication
- Secure network protocols
- Software integrity
- Data protection
- Cybersecurity

---

# 📁 Repository Structure

\`\`\`
discrete-mathematics-in-cryptography/
│
├── README.md
│
├── report/
│   ├── Discrete_Mathematics_in_Cryptography.pdf
│   └── Discrete_Mathematics_in_Cryptography.docx
│
├── presentation/
│   └── Discrete_Mathematics_in_Cryptography.pptx
│
├── diagrams/
│   ├── cryptography-flow.png
│   ├── modular-arithmetic.png
│   ├── rsa-key-generation.png
│   ├── rsa-example.png
│   ├── diffie-hellman.png
│   ├── finite-fields.png
│   ├── aes.png
│   └── hashing.png
│
├── examples/
│   ├── rsa-example.md
│   ├── modular-arithmetic.md
│   └── euclidean-algorithm.md
│
└── references/
    └── references.md
\`\`\`

---

# 📄 Project Documentation

The detailed academic report contains explanations, mathematical derivations, diagrams, worked examples, applications, and references.

The repository is intended to keep the **academic report, presentation, mathematical examples, and supporting material** together in one place.

---

# 🎓 Learning Outcomes

By completing this project, the following connection becomes clear:

\`\`\`
Discrete Mathematics
        ↓
Mathematical Structures
        ↓
Cryptographic Algorithms
        ↓
Security Assumptions
        ↓
Secure Digital Communication
\`\`\`

The project demonstrates that concepts such as modular arithmetic, number theory, algebra, logic, probability, and computational complexity are not merely theoretical topics. They form part of the mathematical foundation of practical computer security.

---

# 💡 Key Takeaway

Cryptography is not simply the process of hiding information.

It is an application of mathematical structures and computational principles.

\[
\boxed{
\text{Number Theory}
+
\text{Algebra}
+
\text{Logic}
+
\text{Probability}
+
\text{Computational Complexity}
}
\]

provide important foundations for understanding modern cryptographic systems.

As computing technology changes, the mathematical assumptions behind cryptography must also be continuously examined and, when necessary, replaced with new approaches.

---

## 👨‍💻 Author

**Tushar Jha**  
B.Tech — Computer Science & Engineering  
Bharati Vidyapeeth's College of Engineering, Delhi

---

## 📚 References

See [\`references/references.md\`](./references/references.md) for the project's reference list and external resources.

---

## ⭐ About This Repository

This repository contains an academic exploration of the relationship between **Discrete Mathematics and Cryptography**, prepared as a B.Tech CSE project.

If you find the project useful for learning, feel free to explore the mathematical examples and supporting documentation.
