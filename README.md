# C++ Feedforward Neural Network

![CI](https://github.com/ana-stanojevic/cpp-ffn/actions/workflows/cpp-ci.yml/badge.svg?branch=main)
![C++](https://img.shields.io/badge/C++-20-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

Neural network implementation with full control over gradients and updates.

This repository focuses on one constraint:  
**the learning process must be fully observable and inspectable.**

Instead of relying on autodiff, gradients are implemented explicitly, making every step of the forward and backward pass visible.

---

---

## System overview

- Feedforward neural network implemented in C++ (Eigen)
- Explicit forward and backward passes
- Manual gradient computation (no autodiff)
- Full access to weights, activations, and updates
- Designed for debugging, inspection, and numerical correctness

---

## Why this exists

Modern ML frameworks hide most of the learning process behind abstraction layers.

While efficient, this makes it difficult to:
- inspect gradient flow  
- debug instability  
- understand how updates propagate  

This system removes that abstraction.

---

## Core idea

> If you can’t inspect the gradients, you don’t control the system.

Gradients are computed manually, making it possible to:
- trace errors step by step  
- verify numerical behavior  
- debug training dynamics precisely  

---

## Architecture

input
↓

linear layers
↓

activations
↓

loss
↓

manual backward pass
↓

gradient updates

---

## System properties

- **Full gradient visibility**
- **No hidden autodiff graph**
- **Deterministic updates**
- **Inspectable forward and backward passes**
- **Built for debugging and correctness, not abstraction**

---

## What this repo demonstrates

Not model performance.

But control:

- how gradients are actually computed  
- how updates propagate through layers  
- where instability originates  
- how to reason about training at a low level  

---

## Tech stack

C++ · Eigen

---

## 👩‍💻 Author

**Ana Stanojevic**  
[Scholar ↗](https://bit.ly/ana-stanojevic) • [CV ↗](https://bit.ly/ana-stanojevic-cv)  

---

## 📜 License  
MIT License — free to use, modify and distribute.  
