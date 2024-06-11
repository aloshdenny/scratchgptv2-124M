# scratchGPTv2

Here is the from-scratch implementation of the 124M GPT-2 architecture from scratch, spelled out in code. I've uploaded the scripts for those who do want get started on pretraining. Any 30 series or above GPU should handle fp16/fp32 training pretty well!

The corpus used is the Edu-FineWeb-10B dataset.

Note that GPT-2 and GPT-3 and both simple language models, trained on internet documents, and all they do is "dream" internet documents. So this repo/video this does not cover Chat finetuning, and you can't talk to it like you can talk to ChatGPT. For now this is the kind of stuff that the 124M model says if you prompt it with "Hello, I'm a language model," after 10B tokens of training:

```
Hello, I'm a language model, and my goal is to make English as easy and fun as possible for everyone, and to find out the different grammar rules
Hello, I'm a language model, so the next time I go, I'll just say, I like this stuff.
Hello, I'm a language model, and the question is, what should I do if I want to be a teacher?
Hello, I'm a language model, and I'm an English person. In languages, "speak" is really speaking. Because for most people, there's
```

Some other lines I tried out:

1. Anish is
```
Anish is a term used to describe the condition of an individual who has been diagnosed with autism. Autism
```

2. what is 1+1?
```
what is 1+1?
The answer to this question depends on the context. For example, if you are talking about a person who has been diagnosed with cancer and have not yet received treatment for it or someone whose symptoms do
```

3. paris
```
paris, the capital of Greece.
The city is located in the heart of the Aegean Sea
```

Apparently GPT-2 is quite bad at math and geography. The reason is becuase GPT-2 is a decoder-only model and only fares at text generation/completion. It does not generate completely new information, rather its wholly autoregressive nature finishes your sentences.

## Video

[Let's reproduce GPT-2 (124M) YouTube lecture](https://youtu.be/l8pRSuU81PU)
