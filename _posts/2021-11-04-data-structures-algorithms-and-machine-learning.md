---
toc: false
layout: post
comments: true
hide: true
description: I'm trying to organize my thoughts on some machine learning research I've seen that combines algorithms and/or data structures with machine learning.
categories: [notes,research]
title: Data structures, algorithms and machine learning
image: /images/dsaml/tn.png
---

  

In Computer Science, algorithmic reasoning has been used to solve problems using predefined sequences of steps and for long have been the default problem solving approach. Machine learning are another approach to problem solving where instead of manually defining a sequence of steps to solve the problem, we learn a functional representation of the solution from the data. Algorithms are fundamentally very different from machine learning models, especially deep neural networks. Those differences means we can use one to improve the other. In this article I will list a few papers I have read recently that combine algorithms or data structures with machine learning.

## Neural Algorithmic Reasoning

The first paper on this list is position paper by DeepMind researcher Petar Veličković and Charles Blundell. It makes a case for building neural networks that execute algorithms. The objective in doing so is to have neural networks gain the advantages of algorithms such as trivial generalization while keeping the advantages of deep learning. Let's have a look at the benefits and limitations of each:
- algorithms: they generalize trivially to any input that fits the right requirements. They are limited by how inflexible they are. Algorithms do not always run on the natural input. The input has to match a specific format, and might require preprocessing that loses information. The real life information would not be accurately represented anymore. 
- deep neural networks: they can deal with natural input and can handle variations of the input. Depending on the type of inductive bias the model has built in, it would be able to handle noise relatively well. Neural networks also have several issues including not being able to do simple reasoning task such as sorting in a reliable way, as well as issues with generalization. 

So how do you get the best of both world? One approach the paper presents consists in having neural networks trained to execute the algorithms step by step. The network can consist of an encoder-processor-decoder sequence where the input is projected onto a latent space where the algorithm like "processing" happens before being decoded into output values. Such an approach was successfully used to learn graph algorithms. #cite Neural Execution of Graph Algorithms.

## Learning Graph Structure With A Finite-State Automaton Layer 