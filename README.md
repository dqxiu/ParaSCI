# ParaSCI
This repo contains downloading instructions for the **ParaSCI** dataset 
in [《ParaSCI: A Large Scientific Paraphrase Dataset for Longer Paraphrase Generation》](https://arxiv.org/pdf/tobeuploaded) along with the code to reproduce results in the paper. 

## Introduction
A paraphrase is a restatement of meaning with different expressions. Being very common in our daily language expressions, it can also be applied to multiple downstream tasks of NLP, such as generating diverse text or adding richness to a chatbot. 

We propose ParaSCI, the first large-scale paraphrase dataset in the scientific field, including 33,981 paraphrase pairs from ACL (ParaSCI-ACL) and 316,063 pairs from arXiv (ParaSCI-arXiv). 

Digging into characteristics and common patterns of scientific papers, we construct this dataset though intra-paper and inter-paper methods, such as collecting citations to the same paper or aggregating definitions by scientific terms. To take advantage of sentences paraphrased partially, we put up PDBERT as a general paraphrase discovering method. 

The major advantages of paraphrases in ParaSCI lie in the prominent length and textual diversity, which is complementary to existing paraphrase datasets. ParaSCI obtains satisfactory results on human evaluation and downstream tasks, especially long paraphrase generation. 


### Detailed Statistics for ParaSCI


| Name | Source | Size (pairs) | Gold Size (pairs) | Len | Char Len | Self-BLEU |
| - | - | - | - | - | - | - |
| ParaSCI-ACL  | ACL Anthology & S2ORC | 59,402 | 33,981 | 19.10 | 113.76| 26.52 | 
| ParaSCI-arXiv | ArXiv Bulk Data & S2ORC| 479,526 | 316,063 | 18.84 | 114.46| 29.90 | 



## Download the Dataset

The main folder `Data` contains training/valid/test sets, each of which is made up by the following files:
```
├──Data
      └── ParaSCI-ACL 
            └── train         // including 28,883 paraphrase pairs
              └── train.src
              └── train.tgt
            └── val           // including 2,753 paraphrase pairs
              └── train.src
              └── train.tgt
            └── test          // including 2,345 paraphrase pairs
              └── train.src
              └── train.tgt
      └── ParaSCI-arXiv
             └── train        // including 309,834 paraphrase pairs
              └── train.src
              └── train.tgt
            └── val           // including 3,680 paraphrase pairs
              └── train.src
              └── train.tgt
            └── test          // including 2,549 paraphrase pairs
              └── train.src
              └── train.tgt

// Each line of *.src is a sentence which paraphrases the sentence in the same line of *.tgt.
// The dataset segmentation of experiments in our paper is different from this, specifically, at a ratio of 6:2:2. However, considering the common segmentation ratio of deep learning experiments, we split the final released dataset at a more appropriate ratio.

```

· Len represents the average number of words per sentence and Char Len represents the average number of characters per sentence. 

· We calculate Len, Char Len and Self-BLEU of the gold-standard paraphrases rather than the whole size of sentences.

---

## Code
We will upload the code as soon as possible.
