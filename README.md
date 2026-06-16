# english-to-tanglish-translator


A fine-tuned Llama language model for English to Tanglish translation using efficient LoRA adapters.
 
## Overview
 
This project fine-tunes a Llama model specifically for translating English text to Tanglish (Tamil-English code-mixed text). It uses **Unsloth** for memory-efficient training with LoRA adapters, requiring minimal computational resources.
 
## Features
 
- **Efficient Training**: LoRA adapters reduce trainable parameters to 1-10% of the full model
- **Memory Optimized**: Unsloth framework dramatically reduces memory usage
- **Fast**: Trained in ~95 minutes on GPU
- **Specialized**: Fine-tuned specifically for English to Tanglish translation
## Memory Efficiency
 
Thanks to **Unsloth**, this project achieves impressive memory optimization:
 
| Metric | Value |
|--------|-------|
| Training Time | 94.99 minutes |
| Peak Memory Used | 6.631 GB |
| Peak Memory for Training | 0.783 GB |
| Memory Usage % | 44.96% of max |
| Training Memory % | 5.31% of max |
 
**Key Insight**: Only **0.783 GB** (5.31%) of peak memory was needed for actual training, thanks to Unsloth's optimization!
 
## Requirements
 
```bash
pip install unsloth
pip install torch
pip install datasets
pip install trl
pip install huggingface-hub
```
 
## Dataset
 
Uses the [English to Tanglish Translation Dataset](https://huggingface.co/datasets/peteparker456/english-to-tanglish-translation-dataset) from Hugging Face.
 
## Usage
 
1. **Setup**: Install dependencies from `requirements.txt`
2. **Train**: Run the notebook cells to fine-tune the model
3. **Save**: Model is saved both locally and pushed to Hugging Face Hub
4. **Inference**: Use the trained model for translation tasks
## Model Details
 
- **Base Model**: Llama
- **Training Method**: Supervised Fine-Tuning (SFT)
- **Fine-tuning Technique**: LoRA (Low-Rank Adaptation)
- **Framework**: Unsloth + TRL (Transformers Reinforcement Learning)
## Output
 
Trained model: `peteparker456/llama-unsloth` on Hugging Face Hub
 
## Why Unsloth?
 
Unsloth enables training large language models on consumer-grade GPUs by:
- Reducing memory footprint by ~70%
- Maintaining training quality
- Speeding up training iterations
- Making LLM fine-tuning accessible
 
## Author
 
Fine-tuned translation model based on the English-Tanglish translation dataset.
 
---
 
**For questions or improvements, feel free to open an issue or submit a PR!**
