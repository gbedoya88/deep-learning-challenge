# deep-learning-challenge


**Analysis** 

In this Analysis I created a tool that can help select applicants for funding with the best chance of success.There we three different optimization models created to achieve a target predictive accuracy higher than 75%. Here are the results.


- Optimization 1 
Dropped an additional column 'USE_CASE'
Created more bins for rare occurances <2000
- Results:
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━┓
┃ Layer (type)                    ┃ Output Shape           ┃       Param # ┃
┡━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━┩
│ dense (Dense)                   │ (None, 80)             │         2,720 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ dense_1 (Dense)                 │ (None, 30)             │         2,430 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ dense_2 (Dense)                 │ (None, 1)              │            31 │
└─────────────────────────────────┴────────────────────────┴───────────────┘
 Total params: 5,181 (20.24 KB)
 Trainable params: 5,181 (20.24 KB)
 Non-trainable params: 0 (0.00 B)
Epoch 100/100
Loss: 0.5681091547012329, Accuracy: 0.7217492461204529






- Optimization 2 
Added more neurons to a hidden layer - layer1=100, layer2=60,layer3=40
Added more layers 'layer 3'
- Results:
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━┓
┃ Layer (type)                    ┃ Output Shape           ┃       Param # ┃
┡━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━┩
│ dense_3 (Dense)                 │ (None, 100)            │         3,400 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ dense_4 (Dense)                 │ (None, 60)             │         6,060 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ dense_5 (Dense)                 │ (None, 40)             │         2,440 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ dense_6 (Dense)                 │ (None, 1)              │            41 │
└─────────────────────────────────┴────────────────────────┴───────────────┘
Total params: 11,941 (46.64 KB)
Trainable params: 11,941 (46.64 KB)
Non-trainable params: 0 (0.00 B)
Epoch 100/100
Loss: 0.5764859318733215, Accuracy: 0.723498523235321



-Optimization 3
Used different activation functions for hidden layers - tanh, tanh, sigmoid
Added the number of epochs - 150
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━┓
┃ Layer (type)                    ┃ Output Shape           ┃       Param # ┃
┡━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━┩
│ dense_7 (Dense)                 │ (None, 80)             │         2,720 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ dense_8 (Dense)                 │ (None, 30)             │         2,430 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ dense_9 (Dense)                 │ (None, 1)              │            31 │
└─────────────────────────────────┴────────────────────────┴───────────────┘
Total params: 5,181 (20.24 KB)
Trainable params: 5,181 (20.24 KB)
Non-trainable params: 0 (0.00 B)
Epoch 150/150
Loss: 0.5666326880455017, Accuracy: 0.7239649891853333



- Summary
Optimization 3 achieved the best performance with the lowest lost 0.56 and the highest accuracy 0.72.
The use of different activation functions as well as the increased epochs likely contributed to better learning and performance.

The model 2 Optimization did not significantly improve performance so that the other layers and neurons did not provide a huge benefit for the specific problem.


To solve the same problem we could use the 'Random Forest' model.

Helps with overfitting decision trees and networks and can also handle both categorical numerical features.
















