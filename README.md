# Neural Network Using Numpy

This projects implements neural nets using numpy library to train MNIST dataset to recognize handwritten digits. The dataset contains 20K , 10K images sets for training and testing scenarios respectively.
Depening on the size of images (28X28), the NN implemented in this project contains 784 neurons at the input layer, and 10 neurons at the output layer. The following key terms are taken into considerations in implementing the project:
  - [x] Hot-encoding is used to represent output labels.
  - [x] Sigmoid function is used as activation function.
  - [x] Stochastic Descenet Gradient for updating weights and biases

> [!NOTE]
> For this network 1-hidden layer is used with 30 neurons. Readers can try with different sets for the parameters of the net including number of layers, size of each layer.


+-----------------------+-----------------------+-----------------------+
| **1.**                | > **Task 1**          |                       |
+=======================+=======================+=======================+
|                       | 1.1.                  | > In your own words,  |
|                       |                       | > describe the main   |
|                       |                       | > differences and     |
|                       |                       | > possible benefits   |
|                       |                       | > of the two          |
+-----------------------+-----------------------+-----------------------+

> algorithms (\~1/4 page)
>
> 1.2. For the Mealy machine below, define (S, s0, ∑, Ω)
>
> S = { a ,b ,c}
>
> s0 = a
>
> ∑= {receiveApplication, documentsComplete, documentsIncomplete}
>
> Ω = {OK , NOK, DONE}
>
> 1.3. For the same Mealy machine, produce the final observation table
> by applying the
>
> L\*M algorithm, and explain the steps involved (\~1/4 page)
>
> a\. Initializing Sp as { } and D as ∑results in the observation table
> in below:
>
> b\. As it is shown in the table, the observation table is not closed
> since the

row for the prefix "receiveApplication" does not match the row ofϵ. This

results in expanding Sp by 'receiveApplication' and the Lp accordingly.

c\.

+-------------+-------------+-------------+-------------+-------------+
|             |             | > receive   | docum       | > documen   |
|             |             | Application | entComplete | tIncomplete |
+=============+=============+=============+=============+=============+
| > Sp        | ϵ           | OK          | OK          | OK          |
+-------------+-------------+-------------+-------------+-------------+
|             | > receive   | OK          | OK          | NOK         |
|             | Application |             |             |             |
+-------------+-------------+-------------+-------------+-------------+
|             | > r         | NOK         | OK          | NOK         |
|             | eceiveAppli |             |             |             |
|             | cation•rece |             |             |             |
|             | iveApplicat |             |             |             |
|             | ion•receive |             |             |             |
|             | Application |             |             |             |
+-------------+-------------+-------------+-------------+-------------+
|             | > rece      | DONE        | DONE        | DONE        |
|             | iveApplicat |             |             |             |
|             | ion•receive |             |             |             |
|             | Application |             |             |             |
|             | •receiveApp |             |             |             |
|             | lication•re |             |             |             |
|             | ceiveApplic |             |             |             |
|             | ation•docum |             |             |             |
|             | entComplete |             |             |             |
+-------------+-------------+-------------+-------------+-------------+
| > *Lp*      | > receive   | NOK         | OK          | NOK         |
|             | Application |             |             |             |
+-------------+-------------+-------------+-------------+-------------+
|             | > docum     | OK          | OK          | OK          |
|             | entComplete |             |             |             |
+-------------+-------------+-------------+-------------+-------------+
|             | > documen   | OK          | OK          | OK          |
|             | tIncomplete |             |             |             |
+-------------+-------------+-------------+-------------+-------------+
|             | rece        | NOK         | OK          | NOK         |
|             | iveApplicat |             |             |             |
|             | ion•receive |             |             |             |
|             | Application |             |             |             |
+-------------+-------------+-------------+-------------+-------------+
|             | > re        | DONE        | DONE        | DONE        |
|             | ceiveApplic |             |             |             |
|             | ation•docum |             |             |             |
|             | entComplete |             |             |             |
+-------------+-------------+-------------+-------------+-------------+
|             | > rece      | OK          | OK          | OK          |
|             | iveApplicat |             |             |             |
|             | ion•documen |             |             |             |
|             | tIncomplete |             |             |             |
+-------------+-------------+-------------+-------------+-------------+
|             | >           | DONE        | DONE        | DONE        |
|             |  receiveApp |             |             |             |
|             | lication•do |             |             |             |
|             | cumentCompl |             |             |             |
|             | ete•receive |             |             |             |
|             | Application |             |             |             |
+-------------+-------------+-------------+-------------+-------------+
|             | receiveAp   | DONE        | DONE        | DONE        |
|             | plication•\ |             |             |             |
|             | documentCom |             |             |             |
|             | plete•docum |             |             |             |
|             | entComplete |             |             |             |
+-------------+-------------+-------------+-------------+-------------+
|             | >           | DONE        | DONE        | DONE        |
|             |  receiveApp |             |             |             |
|             | lication•do |             |             |             |
|             | cumentCompl |             |             |             |
|             | ete•documen |             |             |             |
|             | tIncomplete |             |             |             |
+-------------+-------------+-------------+-------------+-------------+

+-----------------------+-----------------------+-----------------------+
| **2.**                | > **Task 2**          |                       |
+=======================+=======================+=======================+
|                       | 2.1.                  | > A                   |
+-----------------------+-----------------------+-----------------------+

> 2.2.
