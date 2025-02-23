# Dropout Predictor Model

## Problem statement

Student dropout is a significant issue in Rwanda’s higher education sector, influenced by financial, academic, and personal challenges. Existing research underscores the need for context-specific, predictive approaches to address dropout risks in Rwanda. For instance, a study on school dropout and students' academic performance in Rwanda highlights the impact of dropout rates on educational productivity. This Model aims to bridge the gap by incorporating Rwanda-specific data and providing a solution for educators and policymakers.


Training instance
Optimizer used(Adam, RMSPoP)
Regularizer Used(L1 and L2)
Epochs
Early Stopping
( Yes or No)
Number of Layers
Learning Rate
F1 score
Accuracy
 Recall
Precision
Instance 1
Not used
Not used
100
No
3
Not used
class 0(0.92), class 1(0.79)
0.88073
class 0(0.95), class 1(0.73)
class 0(0.88), class 1(0.87)
Instance 2
Adam
Not used
300
Yes
3
0.0001
class 0(0.92), class 1(0.80)
0.88440               
class 0(0.95), class 1(0.73)
class 0(0.89), class 1(0.88)
Instance 3
Adam
L2, 0.001
300
Yes
3
0.0001
class 0(0.92), class 1(0.79)
0.88073
class 0(0.95), class 1(0.73)
class 0(0.89), class 1(0.87)
Instance 4
RMSprop
L2, 0.001
500
Yes
3
0.0001
class 0(0.91), class 1(0.78)
0.87155
class 0(0.95), class 1(0.71)
class 0(0.88), class 1(0.86)

