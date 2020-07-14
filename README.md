# Hierarchical classification

The purpose of this project was to implement from scratch and  compare alteranative approches of hierachical classfication: LCN, LCPL, LCPN, Big-Bang.  

Hierarchical F-SCORE meassure was derived from [sklearn-hierarchical-classification](https://github.com/globality-corp/sklearn-hierarchical-classification).

## Outcomes
#### LCPL
##### Drawbacks:
- at the next level relative to the given LCPL can make predictions of children not belonging to the node with the highest prediction at the given level
- learning samples are unblanaced
- many classes at a given level - worse quality of prediction
##### Pros:
- a small number of classifiers to learn - equal to the number of hierarchy levels
#### LCPN
##### Pros:
- intuitive, corresponds to common sense classification
##### Drawbacks:
- more classifiers from LCPL
#### LCN:
##### Pros:
- it's easy to extend it to multilabel classification 
##### Drawbacks:
- only limited classifiers can be used - those that return confidence in binary classification
- inconsistencies may be obtained with multi-label classification, e.g. simultaneous detection of a cat and a horse
- many local classifiers to learn = long learning time
#### Big Bang:
##### Pros:
- in the simplest case, you can base it on a decision tree 
##### Drawbacks:
- HC4.5 algorithm, hardly described in the literature, relatively difficult to implement
