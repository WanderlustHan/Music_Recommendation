# Title
Music Recommendation for Infrequent Users

# Challenge
Some users barely listen musics. Sometimes it's not because they don't like music, but it's hard for them to obtain musics that satisfy their taste. This scenerio is caused by the lack of training data for this kind of user, which cannot be well solved by the method that is focused on unbalance problem. And it also cannot be sovled by the algorithm which is targeted at cold-start problem, as users in this scenerio are not new users without training data.

# Solution
We don't propose a method to directly sovle this problem.（If we can, it's the best.) We propose a method which could refine existing methods that cannot recommend well for infurequent users. 


* We try to combine Graph Convolutional Networks(GCNs) and Matrix Factorization(MF) to solve this problem. The GCNs are only applied on users to get the information of frequent users. The assumpation under this framework is that, users will listen musics that are listened by the users who are similar as them. 
We use embeddings of existing methods as input to our framework and get a new ranking scores of all items for the infrequent users.
* We use Laplacian regularization to solve this problem.

# Baselines
BRPMF

Caser

SLIM

