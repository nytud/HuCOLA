# HuCOLA
This is the home repository for the Hungarian Corpus of Linguistic Acceptability, which is also part of the Hungarian Language Understanding Evaluation Benchmark Kit ([HuLU](hulu.nlp.nytud.hu)). 

## Data

The files are in the 'data' folder. The dataset contains 9 076 sentences. Each sentence is labelled for its acceptability / grammaticality (0/1).

The sentences were collected by two human annotators from three linguistic books: 
- Kiefer Ferenc (szerk.) (1992), Strukturális magyar nyelvtan 1. Mondattan. Budapest, Akadémiai Kiadó. 
- Alberti, Gábor and Laczkó, Tibor (eds) (2018), Syntax of Hungarian Nouns and Noun Phrases. I., II. Comprehensive grammar resources. Amsterdam University Press, Amsterdam. 
- Katalin É. Kiss and Veronika Hegedűs (eds) (2021), Postpositions and Postpositional Phrases. Amsterdam: Amsterdam University Press.

Each sentence was annotated by four human annotators. The final label of the sentence is the one assigned by the majority of the annotators.

The proportion of train, validation and test sets is 80% (7276 sentences), 10% (900 sentences) and 10% (900 sentences), respectively, following the proportion of the English Corpus of Linguistic Acceptability (as in the GLUE benchmark). The test set is distributed without the labels; to evaluate your model please contact us (ligeti-nagy.noemi@nytud.hu) or visit [HuLU's website](hulu.nlp.nytud.hu) for an automatic evaluation (under construction). The metric of the evaluation is Matthew's Correlation Coefficient.

## Data format

The data files are in json format. The keys are the following:

`sent_id`: unique id of the sentences; it contains the given sentence's split ('train_...', 'test_...', 'val_....') and an integer;

`sent`: the sentence;

`sent_label`: 0 or 1, indicating a wrong (unacceptable, ungrammatical) or good (acceptable, grammatical) sentence, respectively. 

## Guidelines

The annotation guide for the collection of sentences and for the annotation of the sentences are in the 'guidelines' folder.

## License and usage

The corpus is available under the license CC-BY-SA 4.0. If you use this corpus, please cite our paper (see below).

## Citation

If you use this resource or any part of its documentation, please refer to:

Ligeti-Nagy, N., Ferenczi, G., Héja, E., Jelencsik-Mátyus, K., Laki, L. J., Vadász, N., Yang, Z. Gy. and Váradi, T. (2022) HuLU: magyar nyelvű benchmark adatbázis kiépítése a neurális nyelvmodellek kiértékelése céljából [HuLU: Hungarian benchmark dataset to evaluate neural language models]. XVIII. Magyar Számítógépes Nyelvészeti Konferencia. (in press)


```
@inproceedings{ligetinagy2022hulu,
  title={HuLU: magyar nyelvű benchmark adatbázis kiépítése a neurális nyelvmodellek kiértékelése céljából},
  author={Ligeti-Nagy, N. and Ferenczi, G. and Héja, E. and Jelencsik-Mátyus, K. and Laki, L. J. and Vadász, N. and Yang, Z. Gy. and Váradi, T.},
  booktitle={XVIII. Magyar Számítógépes Nyelvészeti Konferencia},
  year={2022}
}
```
