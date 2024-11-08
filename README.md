# Neural Network Using Numpy

This projects implements neural nets using numpy library to train MNIST dataset to recognize handwritten digits. The dataset contains 20K , 10K images sets for training and testing scenarios respectively.
Depening on the size of images (28X28), the NN implemented in this project contains 784 neurons at the input layer, and 10 neurons at the output layer. The following key terms are taken into considerations in implementing the project:
  - [x] Hot-encoding is used to represent output labels.
  - [x] Sigmoid function is used as activation function.
  - [x] Stochastic Descenet Gradient for updating weights and biases

> [!NOTE]
> For this network 1-hidden layer is used with 30 neurons. Readers can try with different sets for the parameters of the net including number of layers, size of each layer.




# Task 1
#### 1.1 In your own words, describe the main differences and possible benefits of the two algorithms (~1/4 page)
- In L<sup>&ast;</sup><sub>M</sub> the model is constructed incrementally i.e., in every round the model gets expanding its tree. On the otherhand, in DHC the hypothesis automata is constructed from scratch in each round. At the end of each round in DHC algorithm, the Counterexamples introduce their suffixes to set of distinguishing suffixes D. This leads DHC to have worst algorithm complexity compared to L<sup>&ast;</sup><sub>M</sub>.
- In DHC, all suffixes to Counterexample is added to D, whereas in L<sup>&ast;</sup><sub>M</sub> exactly one suffice of each CounterExample is added, which relieves the complexity burden to unneccessary membership queries.
- Benefits: DHC is more simple and eases hypothesis construction, on the otherhand L<sup>&ast;</sup><sub>M</sub> with the repetitive tasks of optimization process gets complicated. In addition, L<sup>&ast;</sup><sub>M</sub> converges faster compared to HDC.
#### 1.2 For the Mealy machine below, define (S, s0, ∑, Ω)
      S   = { a ,b ,c}
      s0  = a
      ∑  = {receiveApplication, documentsComplete, documentsIncomplete}
      Ω  = {OK , NOK, DONE}

#### 1.3 For the same Mealy machine, produce the final observation table by applying the L*M algorithm, and explain the steps involved (~1/4 page)
Steps: <br />
- A) Initializing Sp as {} and D as ∑, result in observation table containing the Sp {1} and Lp {A,B,C}.  <br />
- B) The row Lp{A} does not match SP{1}, thus Sp expanded by ‘receiveApplication’ and the Lp accordingly. <br /> &nbsp; &nbsp; &nbsp; Resulting in Sp {1 ,2}, Lp {A,B,C,D,E,F}.  <br />
- C) Lp {D,E} does not match with Sp {1,2}. This further expands Sp by Lp {D}, forming Sp {1,2,3}, and Lp {A,B,C,D,E,F,G,H,I}.
- D) Lastly, Lp{E} does not match entry in Sp {1,2,3}; thus, entries updated as Sp{1,2,3,4} and Lp{A,B,C,D,E,F,G,H,I,J,K,L}. This stage having all the rows in Lp matching with rows in SP, the observation table Closed. <br />

| | S.N  |   | receiveApplication  | documentsComplete  |  documentsIncomplete |
|---|---|---|---|---|---|
| Sp| 1  |  &epsi;  | OK  |  OK | OK  |
|   | 2 | receiveApplication  | OK  | OK  |  NOK |
|   | 3 |receiveApplication &bull; receiveApplication &bull; receiveApplication  |  NOK |  OK  | NOK  |
|   | 4|  receiveApplication &bull; receiveApplication &bull; receiveApplication &bull; receiveApplication &bull; documentComplete  | DONE  |  DONE | DONE  |
|Lp |A|$${\color{red} receiveApplication }$$|$${\color{red}NOK }$$|$${\color{red}OK }$$|$${\color{red}NOK}$$ | 
| |B|documentComplete |OK |OK |OK|
| |C|documentIncomplete |OK |OK |OK |
| |D|$${\color{red} receiveApplication &bull; receiveApplication }$$|$${\color{red}NOK}$$ |$${\color{red} OK}$$ | $${\color{red}NOK}$$ |
| |E|$${\color{red} receiveApplication &bull; documentComplete }$$|$${\color{red} DONE }$$| $${\color{red}DONE}$$ | $${\color{red}DONE }$$|
| |F|receiveApplication &bull; documentIncomplete |OK|OK|OK|
| |G|receiveApplication &bull; receiveApplication &bull; receiveApplication | NOK | OK | NOK |
| |H|receiveApplication &bull; receiveApplication &bull; documentComplete |DONE |DONE |DONE|
| |I|receiveApplication &bull; receiveApplication &bull; documentIncomplete| OK  |  OK | OK  |
| |J|receiveApplication &bull; documentComplete &bull; receiveApplication |DONE |DONE |DONE|
| |K|receiveApplication &bull; documentComplete &bull; documentComplete|DONE |DONE |DONE |
| |L|receiveApplication &bull; documentComplete &bull; documentIncomplete|DONE|DONE|DONE|



# Task 2

I have tried to the last minute, unfortunatly my script give me errors. I have added the SUL code in the file tho
