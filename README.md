# Llama2-PEFT-Instruction-Tuning
A lightweight framework for Supervised Fine-Tuning (SFT) of the Llama-2-7b model using Quantized Low-Rank Adaptation (QLoRA) and the Databricks Dolly-15k dataset.

# Llama-2 Parameter-Efficient Instruction Tuning (QLoRA)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-Integrated-ee4c2c)
![HuggingFace](https://img.shields.io/badge/HuggingFace-Transformers-yellow)
![License](https://img.shields.io/badge/Code_License-MIT-green)

A streamlined framework and technical report for performing Supervised Fine-Tuning (SFT) on the **Llama-2-7b** foundation model. This project leverages **QLoRA (Quantized Low-Rank Adaptation)** to achieve highly efficient instruction-tuning on consumer-grade hardware.

## 📌 Project Overview
As Large Language Models scale, full-parameter fine-tuning becomes computationally prohibitive. This project demonstrates how to align a pre-trained autoregressive model to follow complex human instructions using Parameter-Efficient Fine-Tuning (PEFT) techniques. 

The model was fine-tuned using the **Databricks Dolly-15k** dataset to enhance its zero-shot capabilities in brainstorming, classification, closed QA, generation, information extraction, open QA, and summarization.

## 🛠️ Technical Architecture
* **Base Model:** `meta-llama/Llama-2-7b-hf`
* **Fine-Tuning Methodology:** Supervised Fine-Tuning (SFT) via `trl` (Transformer Reinforcement Learning) library.
* **Quantization:** 4-bit NormalFloat (NF4) via `bitsandbytes` to reduce VRAM footprint.
* **Adapter:** LoRA (Low-Rank Adaptation) targeting linear layers to update only a fraction of total parameters.

## 📁 Repository Structure
* `/src`: Contains the main Jupyter Notebooks and Python scripts for data formatting, memory-efficient training, and inference testing.
* `/data`: Includes the prompt-formatted instruction templates derived from the Dolly-15k dataset.
* `/docs`: Contains the detailed research paper and methodology breakdown.

## 🚀 Getting Started

**1. Clone the repository:**

⚖️ License & Acknowledgements
The code in this repository is licensed under the MIT License.

The Databricks Dolly-15k dataset is governed by the Apache License 2.0.

The Llama 2 model weights are subject to the Meta Llama 2 Community License.

Developed by Himanshu Maurya

```bash
git clone [https://github.com/yourusername/Llama2-PEFT-Instruction-Tuning.git](https://github.com/yourusername/Llama2-PEFT-Instruction-Tuning.git)
cd Llama2-PEFT-Instruction-Tuning
