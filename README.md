# K_Transformer

> Tried Integrating Kalmogrov-Arnold Network and Transformer architecture by replacing MLP.

Transformer uses only one encoder-decoder block as of now(can be increased later). 

**Reason behind integration:**

 - The Kolmogorov-Arnold network[^1] has been shown to have better generalization capabilities, meaning it can perform well on unseen data, compared to an MLP with the same number of parameters.

 - Training KAN on new dataset wont affect its ability to predict on the older dataset. Don't know how it can be useful,

 - KANs can approximate any continuous function with arbitrary precision using a three-layer network structure, thanks to the Kolmogorov-Arnold theorem. In contrast, an MLP typically requires a larger number of hidden layers and neurons to achieve similar accuracy.

 - Read one more paper where it is mentioned that Temporal Kolmogorov-Arnold Networks (TKANs) combine the strengths of KANs and recurrent neural networks like LSTMs. This enables TKANs to effectively handle complex sequential patterns and perform multi-step time series forecasting with enhanced accuracy and efficiency.

So, I thought it can be used in NLP Tasks.

[^1]: https://arxiv.org/abs/2404.19756

## Running the code:

Dataset.zip has two files:
 - english.txt
 - kannada.txt
   
Merge.ipynb is the driver code. It imports K_Transformers.py which uses KAN instead of MLP.
KAN.py has all the necessary functions for implementation of Kalmogrov-Arnold Network.

> PS: I need to try the architecture on other language datasets as of now. Only English to Kannada done. (WLP14 en-fr is too big and will need some more time to run)
