# GPT_From_Scratch

## Project Overview

This project features a PyTorch implementation of a simple bigram-based language model using Transformer architecture to predict text sequences based on the dataset from "Tiny Shakespeare". The model is designed to work on CUDA if available, otherwise on CPU.
Requirements

  Python 3.6 or higher
  PyTorch 1.0 or higher
  A CUDA-compatible GPU is recommended for faster performance, but not required.

## File Descriptions

tinyshake.txt: The input text file containing the Tiny Shakespeare dataset.

## Implementation Details

  Data Processing: The script loads text data, creates a character-level vocabulary, and encodes the text into integer sequences. It splits the data into training   and validation sets.
  
  Model Components:
  
    Head: Represents a single head of self-attention.
      
    MultiHeadAttention: Implements multiple attention heads.
      
    FeedForward: A simple linear layer followed by a ReLU activation.
      
    Block: A single Transformer block consisting of multi-head attention followed by a feed-forward network.
      
    BigramLanguageModel: The main language model class encapsulating all the blocks and handling the forward pass and text generation.
      
    Training Loop: Executes a training loop, periodically evaluating the model on the validation set and printing the loss.
    
    Text Generation: Demonstrates generating text based on learned weights after the training process.

Hyperparameters

  Batch size, block size, number of iterations, learning rate, and other model parameters are defined at the top of the script.


## Example Output

  The model will output the loss at specified intervals and print generated text at the end of training.

## Notes

  Adjust the batch size and block size according to your system's memory capability.
  Increasing the number of heads, layers, or embedding dimensions can improve model performance but requires more computational resources.
