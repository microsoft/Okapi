# Okapi: a Large-Scale Human Labeled Dataset for Compositional Generalization in Natural Language Interfaces to Web APIs
This works presents Okapi, a new dataset for Natural Language to executable web Application Programming Interfaces (NL2API). This dataset is in English and contains 22,508 questions and 9,019 unique API calls, covering three domains. We define new compositional generalization tasks for NL2API which explore the models' ability to extrapolate from simple API calls in the training set to new and more complex API calls in the inference phase. Also, the models are required to generate API calls that execute correctly as opposed to the existing approaches which evaluate queries with placeholder values. Our dataset is different than most of the existing compositional semantic parsing datasets because it is a non-synthetic dataset studying the compositional generalization in a low-resource setting. Okapi is a step towards creating realistic datasets and benchmarks for studying compositional generalization alongside the existing datasets and tasks. We report the generalization capabilities of sequence-to-sequence baseline models trained on a variety of the SCAN and Okapi datasets tasks. The best model achieves 15\% exact match accuracy when generalizing from simple API calls to more complex API calls. This highlights some challenges for future research.

### Okapi statistics in comparison to other semantic parsing datasets

| Dataset | #Question | #Queries | #Domains | #Templates | Realistic | 2-grams Jaccard similarity |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| CFQ | 239,357 | 228,149 | - | 34921 | No | 0.04 |
| SCAN | 20,910 | 20,910 | 1 | - | No | 0.39 |
|GeoQuery | 880 | 246 | 1 | 98 | Yes | 0.24 |
| **Okapi** | 22,628 | 9019 | 3 | 1961 | Yes | 0.14 |

### Comparisons of models' performance on SCAN and Okapi datasets with respect to exact match accuracy(%).
| | SCAN | SCAN | Okapi Doc | Okapi Doc | Okapi Email | Okapi Email | Okapi Calendar | Okapi Calendar |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Method\Split | Len | MCD | Length | Program | Length | Program | Length | Program | 
| LSTM+Attention | 14.1 | 6.1 | 0 | 35.1 | 0 | 26.0 | 0 | 34.0 |
| Transformer+Copy | 0 | 0 | 7.14 | 83.2 | 11.2 | 70.5 | 10.6 | 81.8 |
| T5-Base | 14.4 | 15.4 | 15 |31.37 | 14.85 | 41.06 | 13.2 | 25.79 |

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
