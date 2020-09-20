# AggrE
AggrE aggregates context information into entity and relation embedding for konwledge graph completion.

Specifically, we aim to take full advantage of both the entity context and relation context for enhancing the KGC task. Specifically, different from the neighborhood definition in traditional KG topology, for each element in each triplet, we extract the pair composed of the other two elements as one neighbor in its context.
Then we propose an efficient model, named AggrE, to alternately aggregate the information of entity context and relation context in multi-hops into entity and relation, and learn context-enhanced entity embeddings and relation embeddings. Then we use the learned embeddings to predict the missing relation $r$ given a pair of entities $(h,?,t)$ to complete knowledge graphs.

![](https://github.com/joe817/img/blob/master/Aggre.png)
