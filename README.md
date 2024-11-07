# Neural Network Using Numpy

This projects implements neural nets using numpy library to train MNIST dataset to recognize handwritten digits. The dataset contains 20K , 10K images sets for training and testing scenarios respectively.
Depening on the size of images (28X28), the NN implemented in this project contains 784 neurons at the input layer, and 10 neurons at the output layer. The following key terms are taken into considerations in implementing the project:
  - [x] Hot-encoding is used to represent output labels.
  - [x] Sigmoid function is used as activation function.
  - [x] Stochastic Descenet Gradient for updating weights and biases

> [!NOTE]
> For this network 1-hidden layer is used with 30 neurons. Readers can try with different sets for the parameters of the net including number of layers, size of each layer.




# Task 1
### 1.1 In your own words, describe the main differences and possible benefits of the two algorithms (~1/4 page)
### 1.2 For the Mealy machine below, define (S, s0, ∑, Ω)
      S   = { a ,b ,c}
      s0  = a
      ∑  = {receiveApplication, documentsComplete, documentsIncomplete}
      Ω  = {OK , NOK, DONE}

### 1.3 For the same Mealy machine, produce the final observation table by applying the L*M algorithm, and explain the steps involved (~1/4 page)
A) Initializing Sp as {} and D as ∑, result in observation table containing the first row in Sp and first 3 rows in Lp.  <br />
B) As it is shown in the table, the observation table is not closed since the row for the prefix “receiveApplication” does not match the row of &epsi; . This results in expanding Sp by ‘receiveApplication’ and the Lp accordingly. <br />
C) 

|   |   | receiveApplication  | documentsComplete  |  documentsIncomplete |
|---|---|---|---|---|
| Sp  |  &epsi;  | OK  |  OK | OK  |
|   | receiveApplication  | OK  | OK  |  NOK |
|   | receiveApplication &bull; receiveApplication &bull; receiveApplication  |  NOK |  OK  | NOK  |
|   | receiveApplication &bull; receiveApplication &bull; receiveApplication &bull; receiveApplication &bull; documentComplete  | DONE  |  DONE | DONE  |
|Lp   |receiveApplication |<span style="color:blue"> NOK </span>|OK |NOK | 
| |documentComplete |OK |OK |OK|
| |documentIncomplete |OK |OK |OK |
| |receiveApplication &bull; receiveApplication |NOK | OK | NOK |
| |receiveApplication &bull; documentComplete | DONE | DONE | DONE |
| |receiveApplication &bull; documentIncomplete |OK|OK|OK|
| |receiveApplication &bull; documentComplete &bull; receiveApplication |DONE |DONE |DONE|
| |receiveApplication &bull; documentComplete &bull; documentComplete|DONE |DONE |DONE |
| |receiveApplication &bull; documentComplete &bull; documentIncomplete|DONE|DONE|DONE|






