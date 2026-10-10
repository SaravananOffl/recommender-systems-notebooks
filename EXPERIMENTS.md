# Experiment tracker

Record measured results after running an experiment. Keep validation results separate from final test results.

| Date | Experiment / commit | Data split | Seed | Settings | Validation metric | Test metric | Conclusion |
| --- | --- | --- | --- | --- | --- | --- | --- |

For recommendation experiments, record the model, embedding dimension, learning rate, epochs, and metric definition. For vector quantization, also record codebook size, quantization MSE, and code usage. Use the same split when comparing models.
