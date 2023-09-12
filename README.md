# BigSurvey

![](https://img.shields.io/badge/version-v1.0-blue.svg)
![](https://img.shields.io/badge/language-ENG-lightgrey.svg)
[![](https://img.shields.io/badge/license-ODCBy-green.svg)](https://opendatacommons.org/licenses/by/1-0/)
[![](https://img.shields.io/badge/author-@sq-red.svg)](https://stevenlau6.github.io/)


A large-scale dataset for numerous academic papers summarization

Paper [link](https://www.ijcai.org/proceedings/2022/591)

## Download

Download from Google Drive [link](https://drive.google.com/drive/folders/1DNklRVFFH2jayR6JJeHxMjV74oCjWtie?usp=sharing)


## License
BigSurvey is licensed under [ODC-BY](https://opendatacommons.org/licenses/by/1-0/).

When using the BigSurvey dataset in a product or service, or including data in a redistribution, please cite the following paper:

```
@inproceedings{ijcai2022p591,
  title     = {Generating a Structured Summary of Numerous Academic Papers: Dataset and Method},
  author    = {LIU, Shuaiqi and Cao, Jiannong and Yang, Ruosong and Wen, Zhiyuan},
  booktitle = {Proceedings of the Thirty-First International Joint Conference on
               Artificial Intelligence, {IJCAI-22}},
  publisher = {International Joint Conferences on Artificial Intelligence Organization},
  editor    = {Lud De Raedt},
  pages     = {4259--4265},
  year      = {2022},
  month     = {7},
  note      = {Main Track},
  doi       = {10.24963/ijcai.2022/591},
  url       = {https://doi.org/10.24963/ijcai.2022/591},
}
```

## FAQ

Q1: Does each line of src.txt​ and tgt.txt​ files contain the source documents and the target summary, respectively?

A1: Yes

Q2: What is the "story_separator_special_tag"​ in the src.txt files 

A2: "story_separator_special_tag" separates the input documents in each example.

Q3: Where do the abstracts of the reference papers come from?

A3: We collect them from Microsoft Academic Service and Semantic Scholar.

Q4: Why truncate the input documents?

A4: We truncated the reference papers' abstracts to 200 words because the data sources (Microsoft Academic Service and Semantic Scholar, especially the first one) cannot split the abstract and introduction well. In their APIs' responses, some "abs" can be longer than tens of thousands of words. We think the truncation is necessary. Otherwise, the longest reference abstracts will occupy the major content of the inputs, which is unfair to other reference papers. Most papers' abstracts are within 200-300 words. 
