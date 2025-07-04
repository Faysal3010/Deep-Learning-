# Deep-Learning-
একদম করি ভাই! নিচে আমি **Neural Network & RNN সহ সম্পূর্ণ Deep Learning Core Topics**–এর উপর একঝাঁক গুছানো, GitHub-ready Markdown style বাংলায় নোট বানিয়ে দিচ্ছি — যেমনটা তুই GitHub-এর `README.md` ফাইলে রাখতে পারিস 💡

---

# 🧠 Neural Networks - বাংলায় একদম পরিষ্কার নোট (Beginner → Intermediate)

## 📘 Table of Contents

1. [What is Neural Network?](#1)
2. [Neuron, Weight, Bias](#2)
3. [Activation Functions](#3)
4. [Forward & Backward Propagation](#4)
5. [Loss Function (with Examples)](#5)
6. [Optimizers](#6)
7. [Gradient Descent & Weight Update](#7)
8. [Epoch, Batch, Iteration](#8)
9. [ANN vs CNN vs RNN](#9)
10. [RNN - Core Concept](#10)
11. [Use Cases & Example Projects](#11)

---

<a name="1"></a>

## 🧠 1. What is Neural Network?

নিউরাল নেটওয়ার্ক হলো মানুষের মস্তিষ্ক অনুপ্রাণিত এক ধরনের **Machine Learning Algorithm**।
এটা ইনপুট ডেটা নিয়ে, ধাপে ধাপে ফিচার বের করে, একটা output দেয়।

* 👁️‍🗨️ Input Layer → Hidden Layer(s) → Output Layer

---

<a name="2"></a>

## 🔩 2. Neuron, Weight, Bias

### 🎯 Equation:

```
z = w₁·x₁ + w₂·x₂ + ... + b
a = activation(z)
```

| উপাদান | কাজ                       |
| ------ | ------------------------- |
| `x`    | ইনপুট                     |
| `w`    | ওজন: ইনপুটের গুরুত্ব      |
| `b`    | Bias: আউটপুটকে শিফট করে   |
| `a`    | Activation এর পরের Output |

---

<a name="3"></a>

## ⚙️ 3. Activation Function

### 💡 কেন দরকার?

Neural Network যাতে complex decision নিতে পারে — তার জন্য activation function দরকার।

| নাম     | Range                        | ব্যবহার                   |
| ------- | ---------------------------- | ------------------------- |
| Sigmoid | 0 to 1                       | Binary classification     |
| Tanh    | -1 to 1                      | Centered data             |
| ReLU    | 0 to ∞                       | Most common, fast         |
| Softmax | 0 to 1 (probability sum = 1) | Multiclass classification |

---

<a name="4"></a>

## 🔁 4. Forward & Backward Propagation

### 🟩 Forward:

Input → Weighted Sum → Activation → Output

### 🟥 Backpropagation:

Loss → Gradient → Weight Update
📌 Gradient বের করে optimizer কে দেয়

---

<a name="5"></a>

## 📉 5. Loss Function

**Loss Function** বলে দেয় — model কতটা ভুল করছে।

| নাম                       | ব্যবহার                    | Example        |
| ------------------------- | -------------------------- | -------------- |
| MSE                       | Regression                 | Stock price    |
| MAE                       | Regression                 | House price    |
| Binary Cross-Entropy      | Binary classification      | Spam detection |
| Categorical Cross-Entropy | Multi-class classification | Cat/Dog/Horse  |

---

<a name="6"></a>

## ⚙️ 6. Optimizers

Optimizer = **Weights কিভাবে আপডেট হবে** সেটা বলে দেয়।

| নাম     | বৈশিষ্ট্য              |
| ------- | ---------------------- |
| SGD     | Basic version          |
| Adam    | সবচেয়ে জনপ্রিয়, fast |
| RMSProp | ভালো RNN এর জন্য       |
| Adagrad | Sparse data-friendly   |

---

<a name="7"></a>

## 🧮 7. Gradient Descent & Weight Update

### 🎯 Update Formula:

```text
w = w - learning_rate × ∂L/∂w
```

* ∂L/∂w = gradient of loss wrt weight
* learning rate → কতটুকু পরিবর্তন হবে

---

<a name="8"></a>

## 📦 8. Epoch, Batch, Iteration

| শব্দ       | মানে                                             |
| ---------- | ------------------------------------------------ |
| Epoch      | পুরো ডেটাসেট ১ বার train করা                     |
| Batch Size | কতগুলো sample একসাথে train হবে                   |
| Iteration  | একেকটা batch train হওয়া (1 epoch = N iterations) |

🧠 Example:

* ডেটা: 1000 image
* Batch size = 100
  → 1 Epoch = 10 Iteration

---

<a name="9"></a>

## 🤖 9. ANN vs CNN vs RNN

| Network | ব্যবহার               | ধরন             |
| ------- | --------------------- | --------------- |
| ANN     | Simple numeric data   | Static          |
| CNN     | Image, vision tasks   | Spatial pattern |
| RNN     | Language, time-series | Sequential      |

---

<a name="10"></a>

## 🔁 10. Recurrent Neural Network (RNN)

RNN টাইমভিত্তিক (sequential) ডেটা বোঝে। আগের input মনে রাখে।

### 🧠 Equation:

```
hₜ = activation(Wx·xₜ + Wh·hₜ₋₁ + b)
```

### 🔄 ব্যবহার:

* ভাষা (Text)
* স্পিচ
* টাইম সিরিজ (Weather, Stock)

### 🧨 সমস্যা:

* Long-Term dependency ভুলে যায়
* Gradient vanish হয়

📌 সমাধান → LSTM, GRU

---

<a name="11"></a>

## 🧪 11. Example Project Ideas (Practice-Ready)

| প্রজেক্ট                | বর্ণনা                      |
| ----------------------- | --------------------------- |
| Digit Recognizer (CNN)  | ছবির ভিতর সংখ্যা চিনে       |
| Text Generator (RNN)    | বাংলা কবিতা জেনারেশন        |
| Stock Prediction (RNN)  | টাইম সিরিজ forecasting      |
| Movie Review Classifier | Positive/Negative sentiment |
| Next Word Prediction    | "আমি ঢাকা..." → আসছি/গেছি   |

---

## 🎁 Bonus Tips

* ✅ Always normalize input
* ✅ Use ReLU in hidden, Softmax in output
* ✅ Try Adam optimizer first
* ✅ Track training vs validation loss


