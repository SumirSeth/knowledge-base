---
title: "GENAI - Workshop by Data Vistas"
description: "Key notes from the workshop conducted by The Data Alchemist club of Manipal Institute of Tech."
tags: ['coding', 'workshop', 'ai', 'genai', 'llm']
---

# Data Vistas Workshop

## History of Neural Nets

- Neurons:

  - Summations

  - Activation Function

    Inputs ---> Output

- Neural Networks

- Recurrent Neural Networks (RNNs)

- Weights and Biases

- Long-Short term memory (LSTM)

  Gates

  States

- Encoder - Decoder Architecture: (Next Word Prediction)

- E-D Architecture

- Attention Mechanism

- Transformers

- Attention in Transformers:

  - Encoder:

    - Feed Forward
    - ...

  - Decoder

  - Example:

    - The animal didn't cross the road because it was tired.

      You want the attention of "it" to be on "animal" and not other words like "road" etc.

- GPTs by Open AI in 2018.

- BERT by Google Bidirectional Encoder Representations from Transformers.

  - BERT is pre trained on two NLP tasks:
    - Masked language Modeling
    - Next sentence prediction

- DETR: DEtection transformer by Facebook Research.

- RAGS: Retrieval Augmented Generation

## Prompt Engg.

- What is prompt engg?

  Tailoring prompts to get the best output based on the capabilities of the A.I.

  - Understand AI's capabilities.
  - Provide context.
  - Choose right wording/grammer.
  - Frame the task clearly.
  - Specify tone/style.
  - Assign Roles.
  - Test and iterate.

- Types of Prompting:

  - Few Shot / Few Shot COT <sub>(chain of thought)</sub>
  - Zero Shot / Zero Shot COT

- Papers on CoTR <sub>chain of thought reasoning</sub>: :star:

  - Chain of thought prompting Elicits.
  - Automatic chain of thought prompting.
  - Language Models are few shot Learners.

## Advanced Generative Models : GANs - Generative Adversarial Networks

- What are GANs:
  - GANs generate new, realistic data samples by learning from training data.
- Minimax Game: GANs operate as a two player minimax game where the generator and discriminator compete.
  - The generator aims to maximize the discriminator's error ...
- Training the generator - Mastering deception
  - Random Noise Input
  - Generate Samples
- Training the discriminator - Recognizing Authenticity
  - Real Samples.
  - Fake Samples.
  - Loss minimizations.

## Advanced Generative Models : VAEs - Variational Autoencoders

- What are auto encoders:
  - Basically neural nets using in unsupervised learning.
  - Useful in dimenentionality reduction and stuff.
- Limitations of AE:
  - Overfitting Risk
  - Non probabilistic framework
  - Blurry recognition
  - Deterministic Nature
- VAEs
  - Key Idea: Probabilistic Encoding
  - Diverse Output
  - Structured Latent Space
- General Working
  - Encoder: Encodes input into parameters of probability distribution (mean and variance)
  - Latent Space Sampling
  - Decoder
