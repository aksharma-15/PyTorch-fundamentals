# PyTorch-fundamentals
Foundational knowledge of tensors and their operations with PyTorch

# 🚀 PyTorch Fundamentals for Deep Learning

![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![Python 3](https://img.shields.io/badge/python-3.x-blue.svg?style=for-the-badge&logo=python&logoColor=white)
![NVIDIA Tesla T4](https://img.shields.io/badge/GPU-NVIDIA_Tesla_T4-76B900?style=for-the-badge&logo=nvidia&logoColor=white)

## 📌 Overview

Welcome to the foundational blueprint of Deep Learning with PyTorch. As a senior machine learning engineer, I've mentored countless developers transitioning into AI, and the learning curve almost always flattens once you truly master tensor operations. This notebook serves as a rigorous, hands-on introduction to PyTorch fundamentals. 

Before you build complex neural networks, you need to understand the atomic unit of deep learning: **The Tensor**. This repository is designed to give you the muscle memory required to manipulate data efficiently, leverage hardware acceleration, and avoid the most common pitfalls that plague junior engineers.

---

## 🛠️ Environment & Hardware

To replicate the execution environment of this notebook, you will need:
*   **Compute:** Google Colab (Recommended) or a local machine with CUDA support.
*   **Hardware Accelerator:** NVIDIA Tesla T4 GPU (or equivalent) for accelerated tensor operations. 
*   **Driver & CUDA Version:** Designed for environments running CUDA 13.0 and NVIDIA Driver Version>=580.82.07.

---

## 🧠 Key Concepts Mastered

This notebook sequentially breaks down the essentials of PyTorch:

*   **Introduction to Tensors:** Moving from zero-dimensional scalars to multi-dimensional tensors.
*   **Tensor Creation & Initialization:** Generating tensors with random values, ones, zeros, and ranges (`torch.rand`, `torch.zeros`, `torch.ones`, `torch.arange`).
*   **Datatypes & Casting:** Understanding how to explicitly set and cast datatypes (e.g., `float32`, `float16`, `int32`), which is a frequent source of silent bugs.
*   **Tensor Attributes:** Inspecting `.dtype`, `.shape`, and `.device`.
*   **Manipulating Tensors:** Performing element-wise arithmetic and fundamental mathematical operations.
*   **Matrix Multiplication:** The backbone of neural networks. We cover `torch.matmul()`, the `@` operator, the importance of inner-dimension matching, and matrix transposes (`.T`).
*   **Tensor Aggregation:** Utilizing built-in PyTorch functions to find the min, max, mean, sum, and positional indices (`argmin`, `argmax`).
*   **Dimensionality Manipulation:** Reshaping, stacking (`torch.stack`), squeezing (`torch.squeeze`), unsqueezing (`torch.unsqueeze`), and permuting (`torch.permute`) tensors.
*   **NumPy Interoperability:** Bridging PyTorch tensors and NumPy arrays (`torch.from_numpy`, `.numpy()`), while understanding memory sharing semantics.
*   **Reproducibility:** Taking the "random" out of random initializations using `torch.manual_seed()`.
*   **Hardware Acceleration:** Writing robust, device-agnostic code to seamlessly transfer models and tensors between the CPU and GPU.

---

## ⚠️ The "Big 3" Deep Learning Errors

In my experience, 90% of the bugs you will face when building your first PyTorch models boil down to three fundamental mismatches. This notebook explicitly trains you to identify and resolve them:

1.  **Tensors not right datatype:** Trying to multiply a `float32` tensor with an `int32` tensor.
2.  **Tensors not right shape:** The dreaded matrix multiplication error where inner dimensions do not match.
3.  **Tensors not on the right device:** Attempting to compute operations between a tensor on the `cpu` and another on `cuda:0`.

---

## ⚡ Performance Insight: Vectorization vs. Loops

In deep learning, efficiency is not just a preference; it's a requirement. This notebook includes a live benchmark comparing standard Python `for` loops against PyTorch's vectorized matrix multiplication. 
*   **Result:** Vectorized operations (`torch.matmul()`) process calculations significantly faster (down to microseconds) compared to traditional looping structures (milliseconds), making them practically mandatory for production-scale models.

---

## 📝 Practice Exercises

True engineering intuition comes from practice. The notebook concludes with a set of 9 hands-on exercises that test your ability to:
*   Create and manipulate random tensors on the GPU.
*   Execute matrix multiplications with shape corrections.
*   Extract positional minimums and maximums.
*   Enforce reproducibility using CUDA-specific random seeds.
*   Squeeze and restructure complex tensor dimensions.

---

## 🚀 How to Run

1.  Clone this repository or download the `.ipynb` file.
2.  Upload the notebook to Google Colab.
3.  Navigate to `Runtime > Change runtime type` and select `GPU (T4)`.
4.  Run the cells sequentially to build your PyTorch foundation.

---

## 🤝 Contributing

Contributions to improve the examples, add new functions or methods, or fix typos are always welcome. Please feel free to open an issue or submit a pull request!

## Connect with me
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abhay-kumar-sharma-a22a94171)

---

*Happy coding, and trust the math.*
