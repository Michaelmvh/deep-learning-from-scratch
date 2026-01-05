## Core Terms

- Token -
- Inference - the process of using a trained model to make predictions or decisions on unseen data

## Machine Learning

- (Continuous) Diffusion - Diffusion is a process for generating new data, often images, from noise. The model is trained by learning how to gradually de-noise images in the training set.
  - The forward (noising) process works by adding (Gaussian) noise to data until it is completely noise
    - Reverse (denoising) process involves iteratively removing the noise
  - Used for - images, proteins, ...
- Discrete diffusion - a specific type of diffusion, generally used on text, dna sequences, etc. where instead of gaussian noise, the data transitions between discrete states.
  - When thinking of text, you cannot continuously noise a single word, you must completely noise it
  - Forward (noising) - Degrade the input. For text, we may mask (replace) a word with a similar word from our vocabulary or a special mask token
  - Reverse (denoising) - Model iteratively refines the noise until it is a piece of data resembling the training data
- Masked diffusion - An implementation of discrete diffusion where parts of the input are systematically masked until the entire sequence is masked
- Pre training

* Fine tuning
* Post training - includes rl and fine tuning I think
* Confidence module or model?
* Masked diffusion
* Transformer
* Attention
* Contrastive learning
* Embeddings
* Latent Space
* Graph Neural Network
* BERT
* force field energy minimization
* MLP
* Neuron
* CNN
* RNN

Techniques

- Hyperparameter trick
-

## Math

- Gaussian Perturbation - applying a small randomly generated deviation following a gaussian to a system to analyze its response
- Gaussian Distribution - normal distribution
  - Synonyms: Gaussian, normal distribution
- Markov Chains
- Monte Carlo
- Monte Carlo Trees
- Chain rule
- derivatives

## Protein models

- ESM-2 -
- AlphaFold
- AlphaFold2
- AlphaFold3
- RosettaFold
- RFDiffusion
- ProteinMPNN
- LigandMPNN
- AtomWorks
- Protein Data Bank
- Chai-1

Auto-regression vs Text Diffusion

- Auto-regressive Models (ARM) outputs one token at a time based on the previous tokens
  - Small errors can lead to large drift in output
- Text diffusion outputs the entire sequence and iteratively refines it
  - Faster than ARM
  - Can more easily insert text in an existing flow
