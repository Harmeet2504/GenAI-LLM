# GenAI-LLM

Protein language models (PLMs) are powerful tools for understanding and designing proteins using deep learning techniques. They work similarly to natural language models but are trained on protein sequences to predict structures, functions, and interactions or braodly specific phenotypes.This repo is dedicated to using ESM2 models for various tasks. It will be updated periodically. 

Selection of specific model:
In protein language models (PLMs) like ESM-2, specific versions of the trained model that vary in size, complexity, and computational requirements are referred to as checkpoints. Each checkpoint has a different number of layers and parameters, which affect the model's performance, accuracy, and speed. Here's a breakdown of what these mean:
1. Checkpoint Name:
Each checkpoint in ESM-2 follows a naming convention:
- esm2_tX_YB_UR50D
- X = Number of layers (depth of the model).
- YB / YM = Number of parameters in billions or millions (model size).
- UR50D = Dataset used for training (e.g., UniRef50 with deep training).
2. Number of Layers
- More layers generally mean better feature extraction, allowing deeper insights into protein sequences.
- Larger models (e.g., 48 layers) capture more subtle sequence features but require more computational power.
- Smaller models (e.g., 6 layers) are faster and more lightweight, making them suitable for quick experiments.
3. Number of Parameters
- Parameters define how much the model has learned.
- A 15B parameter model (esm2_t48_15B) is extremely large, capable of deep protein representation learning.
- A 6M parameter model (esm2_t6_8M) is much smaller but still useful for basic tasks.
Choosing the Right Checkpoint
- For high-precision tasks (e.g., protein design, fine-tuning) → Use larger models (e.g., esm2_t48_15B).
- For lightweight, faster inference (e.g., quick mutation analysis) → Use smaller models (e.g., esm2_t6_8M).
- For balanced performance → Mid-sized models like esm2_t33_650M work well.


Get started with

Set up a virtual environment and activate it
```
pip install transformers torch biopython