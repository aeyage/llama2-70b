## Meta - Llama 2 70B

${\textsf{\color{lightgrey}Work in Progress}}$

>**Llama2** by Meta is an example of an LLM offered by AWS. Llama 2 is an auto-regressive language model that uses an optimized transformer architecture and is intended for commercial and research use in English. It comes in a range of parameter sizes — 7 billion, 13 billion, and 70 billion as well as pre-trained and fine-tuned variations.

Many AI and ML professionals and practitioners fine-tune or pre-train these Llama 2 models with their own text data to improve accuracy for their specific use case. However, there is one bottleneck - the high cost of fine-tuning and training and I will explore how we can use the *Neuron distributed training library* to fine-tune, continuously pre-train, and reduce the cost of training LLMs such as Llama 2 with *AWS Trainium instances on Amazon SageMaker*. 

## Prerequisites

A Hugging Face access token is required to download the Hugging Face tokenizer to be used later and make a few quota increase requests for SageMaker [8 Trn1 instances - maximum of 32 Trn1 instances depending on time-to-train and cost-to-train trade-offs for your use case].

Request the following SageMaker quotas on the Service Quotas console:

- Trainium instances (ml.trn1.32xlarge) for training job usage: 8–32
- ml.trn1.32xlarge for training warm pool usage: 8–32
- Maximum number of instances per training job: 8–32

Note that it may take up to 24 hours for the quota increase to get approved.

## License

Licensed under the MIT License.
