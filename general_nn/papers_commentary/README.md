### Papers [[Commentary](papers_commentary)]

#### ** Dropout ** 

1. [Dropout:  A Simple Way to Prevent Neural Networks from Overfitting](http://jmlr.org/papers/volume15/srivastava14a/srivastava14a.pdf)   

 This is (I think - it's hard to tell) the canonical paper introducing the concept of dropout in neural networks (an earlier version of the paper can be found in [arxiv](http://arxiv.org/pdf/1207.0580.pdf)). It gives great motivation for the use of dropout, and a good amount of digestible detail on the structure and implementation of a neural network using dropout. It motivates the intuition behind dropout well, and includes some nice visuals to help show what goes on in networks using dropout. 

 My main takeaways are as follows: 

* There are two main motivations for dropout: 
 * Dropout is a technique to help prevent/correct for overfitting. 
 * Dropout allows us to effectively perform model averaging by building loads of thinned networks that have learned different features. 
* It is successful for two reasons: 
 * It leads to less complex networks, which means we are less likely to overfit. 
 * It helps prevent the hidden units in our network from co-adapting, and instead leads to hidden units learning more useful features on their own (e.g. irrespective of what other hidden units are learning). If we look at the activations of the nodes in each layer of the net with and without dropout, we see that with dropout, we have fewer nodes that have high activation (suggesting that fewer nodes are learning at any given time, helping to prevent nodes from co-adapting). 
* It is implemented by randomly dropping out some subset of nodes/neurons in each layer, where we can specify the probability `p` of dropout in each layer.  

[@sallamander](https://github.com/sallamander)