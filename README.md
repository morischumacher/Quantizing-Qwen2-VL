# Quantizing Qwen2-VL: FP16 vs. 8-bit

An experiment on how 8-bit quantization changes the quality, memory use, speed and energy use of a vision-language model. Model: Qwen2-VL 2B. Task: image captioning on COCO 2017 val (5,000 images). Course: Introduction to Computational Sustainability, TU Wien.

Quantization is one of the main levers for running AI models on less hardware and less energy, which makes it a cost question as much as a technical one.

## Approach

- Three setups: an FP16 baseline, 8-bit weights for the language model only, and 8-bit for both the language model and the vision tower.
- Quality measured with BLEU-4 and CIDEr; peak VRAM, throughput, model size and energy tracked per run.

## Tech stack

Python, PyTorch, Hugging Face Transformers and Accelerate, bitsandbytes, sacrebleu, Jupyter

## Files

- [Qwen2VL_Captioning_FP16_vs_INT8.ipynb](Qwen2VL_Captioning_FP16_vs_INT8.ipynb): the whole experiment, from setup and data loading to the comparison charts.
