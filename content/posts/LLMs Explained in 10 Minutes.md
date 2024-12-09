---
title: LLMs Explained in 10 Minutes
draft: false
---
Every day we hear about AI taking over jobs, writing novels, and even passing medical exams. But are these things really that smart? Let's break down exactly how they work - no hype, just clear explanations.

ChatGPT Text prompt: “How many r’s in the word strawberry?

Re-ask: “Think again, and answer carefully”


[Intro]



Disclaimer: This is not going to be a deep dive into all the details, we will rely heavily on intuition, visuals and  simplification for the sake of easier understanding. In reality, things are a bit more complex and have much more math involved.

[“English is the hottest new programming language.” - andrej]

  

AI Landscape

  

Where do LLMs fit in the bigger picture?

  

[Animated Hierarchy Diagram]

- Artificial Intelligence (Machines that can perform "intelligent" tasks)

  - Machine Learning (Systems that learn from data)

    - Deep Learning (Neural networks that can learn complex patterns)

      - Natural Language Processing (Understanding and generating human language)

        - Large Language Models (Advanced text understanding and generation)

  

The goal of Machine Learning is to discover patterns in data.

  
  

Token

To understand LLMs, we first need to know how they see text.

  

A token is a unit of text, it is not equivalent to a word (Although, for convenience ‘word’ and ‘token’ are used interchangeably.) It could be a single character, parts of a word, a whole word, or even a whole phrase. 

  

The sentence “Nothing tops a plain pizza.” might be broken down into [V], it depends on the tokenization method used.

  

Tokenization is the process of breaking down large text into smaller units (tokens) so that it can be processed by LLMs.

  
  

Word embeddings: Giving words meaning

  

Once tokenized, we need a way for LLMs to understand meaning. But computers work with numbers, not words, so we convert words into vectors, a process known as word embedding

  

[Animation showing transformation] w/ a disclaimer of fake vectors

Word: "cat" → Vector: [0.2, 0.1, 0.3]

Word: "dog" → Vector: [0.25, 0.15, 0.28]

Word: "car" → Vector: [0.8, 0.6, 0.1]

  

Words with similar meanings are represented by vectors that are closer together. ‘Cat’ and ‘Dog’ will have vectors closer than ‘Cat’ and ‘Car’.

  

Word embeddings let LLMs capture the relationships between words. This is why, for instance, if you take the vector for 'king,' subtract 'man,' and add 'woman,' you get close to 'queen.'

  

So far, we took  a sentence, broke it into words, and converted  these words into word embeddings, which contain semantic and syntactic meaning embedded within them.

  

Now all these word embeddings or vector embeddings are stored in a vector database.

  
  

The Neural Network

Humans think through language. When we talk to ourselves or think through problems, we don’t always know what we’ll say next; it’s a process unfolding moment-by-moment, it’s like our own inner language model inside the brain.

Like right now, I don’t even know what I’m going to say next… this part was not scripted!

  

At its core, an LLM is a very large neural network.

A neural network is a sequence of many connected layers of ‘neurons.’ Information starts at the input layer, passes through these layers to help predict outcomes, like guessing the next word in a sentence.

[Input: Cat image -> NN -> Output probability chart]

  
  

Large Language Models

  
It is a type of neural network.

  

Large = large number of neurons, also called parameters, in the neural network.

[GPT-4 has X trillion neurons, a human brain has 100 B)

  

Language Model = learn to predict the next word

The input to the model is a string of text, and its goal is to predict the next word based on what it has seen so far. Language modeling, or learning to predict that next word, is the core job of an LLM."

  

[Next word prediction NN Prob char visual]

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcISKO9LTQUcbATrLHBc3VI5IpkgBUGVY8VcEhrDO8HiphMxeFJfxY5XhOyHo2hLr63phdWpq1_Qbpskr3i9aoYR7p4toa0vGv91MiAQnwOMR3sf203BAsB93tF0SwT9jNnb-EQh_4TlqPjksOpTPnXMynO?key=D4_TYKD0aFMwoMQreaJacA)

Input Layer: Receives the embedded words

Hidden Layers: Process the information

Output Layer: Predicts the next word

  
  

Training Process

  

We need to “train” the  neural net to predict the next word. And to do that, we need data, a lot of data.

  

Thanks to the internet, we have a lot of text data: books, articles, code, conversations,  etc. 

  

So we create a massive dataset from the internet. 

  

We feed this massive text dataset into the model, teaching it to predict the next word in all the different contexts, which enables it to handle everything from generating poems to writing code.

  
  

Generative AI

LLMs are an example of Generative AI since they generate new text. But they don’t always just pick the most probable word. Sometimes we want them to be creative, to add a bit of ‘randomness’ to responses. This is done using a setting called Temperature.

A higher temperature means more creative responses, while a lower temperature yields safer, more predictable ones. This is why you might get different answers each time you ask the same question.

  
  

GPT

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXePIVsZ4v0V4GQMTaoGFTy5BXaiGwhQx6MrBZyW67_kZvU-UW-JpqARW2lFoyGJkSfuwXipTG95kPdOnNgLER37W9WP6EHAoS9Um41LG4DOSnn_i6NHEELvL9lrwanDvPnCSaSsM4HEK_VWT0ZYdpsLvWsc?key=D4_TYKD0aFMwoMQreaJacA)

  

G = generative, means  next word prediction

P = pre-trained - first phase of training

- Pre-training - training on a massive, general dataset
    
- Fine Tuning - refining for specific tasks using carefully curated data
    

- Chat in ChatGPT stands for it has been refined for chatting and q and a style output
    

- Reinforcement learning from human feedback (RLHF) - Humans help the model understand which responses are better
    

T = transformer -  
  
[2017] Google deep minds - attention is all you need - The breakthrough that made modern LLMs possible: “Attention”

  
-> transformer architecture is a specific neural network architecture, and it works so well because it can focus its “attention” on the parts of the input sequence that are most relevant at any time and not the whole thing

  

When you read 'The bank is by the river', you know which 'bank' we mean because you pay attention to the context 'river'. In this entire sentence, the only relevant words are ‘bank’ and ‘river’, ‘attention’ is what helps us identify that.

  
  

[“The bank is by the river.”]

[“The bank is by the building.”]

Without attention, the word bank in these two cases  will be embedded in the same way, but after the attention layers, these same words now have the meaning of their context embedded within the vectors.

  
  

Limits of LLMs

LLMs generate human-like text, not true text. They can sometimes ‘hallucinate’—confidently generating incorrect or nonsensical information.

  

So now you understand the basics of how LLMs work. Do you think they are ‘smart’ or ‘magical’?

  

Because all it's doing is predicting the next word one at a time. The magical part is in how well it works.

  

What makes LLMs so useful is, when faced with something they have never seen before, they perform very well. This is also called Zero shot learning.

  

LLMs are limited by the amount of text they can see at once, also known as Context Window.

[Example]

  

We can make the outputs better by providing examples on how to generate the answer. Works amazing when we want a specific output format. Also called Few Shot learning.

  

Now ask the model to think step by step, and the results are significantly better. This is what roughly the new OpenAI o1 models do, they ‘think’ in the background and provide reasoning to the answers generated. This is also called chain-of-thought prompting.

  

This is why in the start, when we asked gpt to think step-by-step, we got the right answer for “how many r’s in a strawberry?”.

  
  

Conclusion

  

Are LLMs actually smart? Well, that is up for debate. Some say, for it to be this incredibly good at next-word-prediction, the LLM must actually acquire an understanding of the word internally.

  

Others argue that the model simply learned to memorize and copy patterns seen during training, and has no actual understanding of language, the world or anything else. This side argues that They're not magic, but they're math. Very impressive math, but still just pattern recognition at an enormous scale.

  

This is also called the ‘Black Box Problem’

The black box problem describes the inability to fully understand or explain how LLMs arrive at their outputs. Despite knowing the general architecture and training process, we cannot trace the exact reasoning path for ‘why’ specific decisions were made by these models.  
  

[Outro]

**