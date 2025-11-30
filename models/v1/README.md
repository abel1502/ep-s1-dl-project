Pretrained text encoder (`camambert`) without finetuning + some metadata fed into a feedforward classifier with 1 hidden layer

<s>Somehow fares worse than logistic regression...? Heck, its public score is the same as dummy classifier...</s>

Oh, nevermind, I see the problem! The code to record the predictions was off. When fixed, this yields a respectable 3.7% improvement over tf-idf + logistic regression. A good first attempt, I'd say.
