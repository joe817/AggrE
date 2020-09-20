# AggrE
AggrE aims to take full advantage of both the entity context and relation context for enhancing the KGC task. Specifically, different from the neighborhood definition in traditional KG topology, for each element in each triplet, we extract the pair composed of the other two elements as one neighbor in its context.
Then we propose an efficient model, named AggrE, to alternately aggregate the information of entity context and relation context in multi-hops into entity and relation, and learn context-enhanced entity embeddings and relation embeddings. Then we use the learned embeddings to predict the missing relation $$r$$ given a pair of entities $$(h,?,t)$$ to complete knowledge graphs.

![](https://github.com/joe817/img/blob/master/Aggre.png)

## Files in the folder

- `data/`
  - `FB15k/`
  - `FB15k-237/`
  - `wn18/`
  - `wn18rr/`
  - `NELL995/`
  - `DDB14/`
- `AggrE_code.ipynb`: implementation of AggrE.

## Basic requirements

* python 3.7.7
* numpy 1.18.5
* tensorflow 1.15.0

Note: you are recommended to run this code on GPU.

##

## Experimental results of relation prediction

| Dataset |  acc | mrr | mr | h1 | h3 | h5 | h10 |
|:---------------:|:---------------:|:---------------:|:---------------:|:---------------:|:---------------:|:---------------:|:---------------:|
|FB15k-237|0.9204| 0.9658 |1.1707|0.9336|0.9894|0.9954|0.9982|
|FB15k|0.4185|0.9826|1.2156|0.9476|0.9922|0.9930|0.9972|
|wn18rr|0.9173|0.9530|1.1358|0.9206|0.9890|0.9951|0.9993|
|wn18|0.6005|0.9921|1.0339|0.9885|0.9954|0.9987|0.9998|
|NELL995|0.7183|0.8509|2.2773|0.7737|0.9162|0.9470|0.9716|
|DDB14|0.9551|0.9728|1.0799|0.9529|0.9917|0.9982|0.9997|
