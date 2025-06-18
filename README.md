# 🍃 Luffa Leaf Disease Detection using CNN & ViT  
> *Plant Disease Detection using Deep Learning | CNN • Vision Transformer • MLP Head Experiments*
---
## 🧭 Start Here — What’s in This Repository?

### Structure

### 1. Root Directory
<table>
  <tr>
    <th>File/Folder</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><code>main_cnn.ipynb</code></td>
    <td>Final CNN model trained on <strong>pathologist-verified data</strong> (2 classes)</td>
  </tr>
  <tr>
    <td><code>main_vit.ipynb</code></td>
    <td>Final ViT model trained on <strong>pathologist-verified data</strong> (2 classes)</td>
  </tr>
  <tr>
    <td><code>cnn_experiments/</code></td>
    <td>CNN trials on <strong>3-class dataset</strong> (unverified)</td>
  </tr>
  <tr>
    <td><code>vit_experiments/</code></td>
    <td>ViT trials on <strong>3-class dataset</strong> (unverified)</td>
  </tr>
</table>

---

### 2. <code>vit_experiments/</code> - Vision Transformer Trials
Experiments are structured based on:
- <strong>MLP Head Variations</strong> (<code>MLP 1</code>, <code>MLP 2</code>, <code>MLP 3</code>, <code>MLP 6</code>, <code>MLP 9</code>)
- <strong>Image Preprocessing</strong> (<code>RAW</code>, <code>320×548px</code>, <code>854×480px</code>, <code>1920×1080px</code>)
- <strong>Patch Sizes</strong> (<code>4×4</code>, <code>6×6</code>, <code>7×7</code>, <code>8×8</code>,  <code>12×12</code>)

<h4>📂 Folder Naming Format:</h4>
<pre><code>Luffa_MLP_[HEAD]_[RESOLUTION]</code></pre>
<ul>
  <li><strong>[HEAD]</strong> → Number of MLP layers (e.g., <code>MLP 2</code> = 2-layer MLP head)</li>
  <li><strong>[RESOLUTION]</strong> → Image preprocessing method:
    <ul>
      <li><code>RAW</code> → Original resolution (no resizing)</li>
      <li><code>320</code> → Resized to 320×548px (using Microsoft PowerToys)</li>
      <li><code>480</code> → Resized to 854×480px(using Microsoft PowerToys)</li>
      <li><code>1080</code> → Resized to 1920×1080px(using Microsoft PowerToys)</li>
    </ul>
  </li>
</ul>

<h4>📄 File Naming Format:</h4>
<pre><code>Luffa_[IMAGE_SIZE]_[PATCH_SIZE]_[EXECUTION TIME]_(VERSION).ipynb</code></pre>
<ul>
  <li><strong>[IMAGE_SIZE]</strong> → Input dimensions (e.g., <code>21×21</code>, <code>64×64</code>)</li>
  <li><strong>[PATCH_SIZE]</strong> → ViT patch size (e.g., <code>7×7</code>, <code>12×12</code>)</li>
  <li><strong>[EXECUTION TIME]</strong> → Random execution time (e.g., <code>4821s</code>)</li>
</ul>

---

## 🧪 What is This Project About?

This is a deep learning research project focused on detecting diseases in *Luffa aegyptiaca* (sponge gourd) leaves.

I used:
- 📸 Leaf images (2 datasets — one verified by a plant pathologist)
- 🧠 CNNs and Vision Transformers (ViTs)
- 🧪 Different image sizes, patch sizes, and MLP heads

The goal: ✅ High-accuracy, low-resource models for field use in agriculture.


---

## 🌱 Dataset Info


🧬 Two datasets used:

| Dataset Version  | Classes                                        | Verified                 | Link                                                          |
| ---------------- | ---------------------------------------------- | ------------------------ | ------------------------------------------------------------- |
| Raw Dataset      | Cucumber Mosaic Virus, Downy Mildew, Leaf Spot | ❌                        | [Mendeley Link](https://data.mendeley.com/datasets/dkptcnjn42/4)|
| Verified Dataset | Mosaic Disease, Insect Infestation             | ✅ (by plant pathologist) | [Mendeley Link](https://data.mendeley.com/datasets/nym8bw5hr6/3) |


📌 All images were resized using PowerToys or custom Python scripts for training on Google Colab CPU.



> 📌 Want to use the dataset? Please cite the Mendeley data links (above).

---

## 🧠 Model Overview

### 🔹 CNN (Convolutional Neural Network)
- Used mostly for `32x32` and `64x64` images
- Implemented in:
  - `cnn_experiments/`
  - `main_cnn.ipynb` (final verified version)

### 🔸 ViT (Vision Transformer)
- Used patching methods like `4x4`, `6x6`, `7x7`,`8x8`
- Tried MLP Head layers like `1`, `3`, `6`, `9`
- Image Sizes tested:
  - `21x21`, `28x28`, `32x32`, `48x48`, `56x56`, `64x64`

---

## 📊 Accuracy Highlights

| Model Notebook                         | Dataset        | Accuracy  | Notes                        |
|----------------------------------------|----------------|-----------|------------------------------|
| `main_cnn.ipynb`                       | 2-class (✅)   | 98.32%     | Final CNN model              |
| `main_vit.ipynb`                       | 2-class (✅)   | 99.85%     | Final ViT model              |
| `Remodeled_CNN_BY_TARIQ_worked.ipynb` | 3-class (⚠️)   | ??     | Older CNN                    |
| `Luffa_32X32_8X8_4821s_(9)3.ipynb`     | 3-class (⚠️)   | 99.65%     | Strong ViT on unverified set |

---

## 🚀 Getting Started

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/luffa-leaf-disease-detection.git
   cd luffa-leaf-disease-detection

2. Launch any .ipynb in Google Colab or Jupyter Notebook

Start with:

main_cnn.ipynb (for 2-class CNN)

main_vit.ipynb (for 2-class ViT)

Or explore cnn_experiments/ and vit_experiments/ for more!

---

## 📚 Citations

Md Tariqul Islam. "Luffa Aegyptiaca Leaf Disease Detection using CNN & Vision Transformer", Mendeley Data.

2-Class Dataset on Mendeley - https://data.mendeley.com/datasets/nym8bw5hr6/3

3-Class Dataset on Mendeley - https://data.mendeley.com/datasets/dkptcnjn42/4


