# Disfluency Detection

Inspired by the finetuning approach showcased in [this blog.](https://ai.googleblog.com/2022/06/identifying-disfluencies-in-natural.html)

This model uses [Disfl-QA](https://arxiv.org/pdf/2106.04016v1.pdf) which aggregates disflenct text as well as cleaned text, allowing us to create a binary classifier that classifies if a given sentence contains disfluency measures or not.

For this approach, [bert-base-uncased](https://huggingface.co/bert-base-uncased) was pretrained on [reddit dataset](https://huggingface.co/datasets/reddit) as this dataset contains a lot of disfluencies generally encountered in speech like self-repitition and self-correction as well it exposes the model to more informal free speech sentence structures. At last the model was finetuned on [Disfl-QA](https://arxiv.org/pdf/2106.04016v1.pdf) dataset using [Adam optimizer](https://arxiv.org/pdf/1412.6980.pdf) for 3 epochs which led to the result of a validation accuracy of 97.95%

The pretrained model can be found [here](https://huggingface.co/kapilchauhan/pretrained-bert-free_speech) while the finetuned model can be found [here](https://huggingface.co/kapilchauhan/fintuned-bert-disfluency)
