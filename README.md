# scratchGPTv2

Here is the 2nd edition of the from-scratch implementation of the 124M GPT-2 architecture, spelled out in code. I've uploaded the scripts for those who do want get started on pretraining. Any 30 series or above GPU should handle bfloat16 precision training pretty well!

<div align="center">
  <img src="image.png" alt="GPT-2 Block Architecture" width="500" style="display: block; margin-bottom: 10px;">
  <p style="margin-top: 0;">GPT-2 Block Architecture</p>
</div>

The corpus used is the Edu-FineWeb-10B dataset.

Note that GPT-2 and GPT-3 are both simple language models, trained on internet documents, and all they do is "dream" internet documents. So this repo does not cover finetuning, and you can't talk to it like you can talk to ChatGPT. For now this is the kind of stuff that the 124M model says if you prompt it with "Hello, I'm a language model," after 10B tokens of training:

```
Hello, I'm a language model, and my goal is to make English as easy and fun as possible for everyone, and to find out the different grammar rules
Hello, I'm a language model, so the next time I go, I'll just say, I like this stuff.
Hello, I'm a language model, and the question is, what should I do if I want to be a teacher?
Hello, I'm a language model, and I'm an English person. In languages, "speak" is really speaking. Because for most people, there's
```

Some other lines I tried out:

1. Happy Birthday Anish
```
Happy Birthday Anish Kapoor
- The Indian National Anthem: “Bhagat Singh”
-
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

Apparently, GPT-2 is quite bad at math and geography. The reason is because GPT-2 is a decoder-only model and it fares better at text completion pipelines. It does not generate completely new information, rather its wholly autoregressive nature finishes your sentences.

## Video

[Let's reproduce GPT-2 (124M) YouTube lecture](https://youtu.be/l8pRSuU81PU)
