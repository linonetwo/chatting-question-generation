# chatting-question-generation 聊天话题生成器

利用互联数据生成聊天话题，先用中文的 CnSchema 搞个原型。Using Linked-Data to generate chatting topic, currently Chinese version only.

(首先使用 Markdown 实现，因为最近在玩歧路旅人没空写代码了。)

## 利用上堆下切平行的方法找话题

「上堆下切平行」详见《[CHUNK-UP CHUNK-DOWN And PARALLEL And Reverse 上堆、下切、平移和逆向](docs/Chunking.md)》里对 NLP 的简要介绍。

具体的实现思路详见 《[Association Of Topics 话题的联想](docs/AssociationOfTopics.md)》，我们将使用 [Data 文件夹](data/Readme.md) 内的 JSON-LD 里定义的上下级关系来实现「上堆下切平行」联想。

## 语言的润色

我们将结合模板方法和神经网络方法来使生成的文本尽可能接近自然交流的语用情况，减轻用户的润色压力。

模板方法将采用[共产中文报告生成器](https://github.com/linonetwo/communism-report-generator)的思路，利用模板生成语句 CST 后序列化成文本。
