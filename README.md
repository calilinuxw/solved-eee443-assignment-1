Download Link: https://assignmentchef.com/product/solved-eee443-assignment-1
<br>
A single neuron receives input from <em>m </em>input neurons with weights <em>w<sub>i</sub></em>, where <em>i </em>∈ [1 <em>m</em>].

The neuron is expected to predict the probability that the output <em>t </em>belongs to <em>Class A </em>(<em>t </em>= 1) versus <em>Class B </em>(<em>t </em>= −1). A datasets of training samples are available with inputs <em>x<sup>n </sup></em>and outputs <em>y<sup>n </sup></em>(<em>n </em>∈ [1 <em>N</em>]). You are told that the maximum a posteriori estimate for the network weights are obtained by solving the following optimization problem:

argmin<sup>X</sup>(<em>y<sup>n </sup></em>− <em>h</em>(<em>x<sup>n</sup>,W</em>))<sup>2 </sup>+ <em>β </em><sup>X<em>w</em></sup><em><sub>i</sub></em><sup>2                                                                                              </sup>(1)

<em>W</em>

<em>n                                                        i</em>

where <em>W </em>is the vector of weights <em>w<sub>i</sub></em>, <em>β </em>is a scalar constant, and <em>h</em>(<em>.</em>) is the output of the neuron. According to this estimate, derive the prior probability distribution of the network weights analytically.

<h1>Question 2.</h1>

An engineer would like to design a neural network with a single hidden layer with four input neurons (with binary inputs) and a single output neuron to implement:

(<em>X</em><sub>1 </sub>OR NOT <em>X</em><sub>2</sub>) XOR (NOT <em>X</em><sub>3 </sub>OR NOT <em>X</em><sub>4</sub>)

Assume a hidden layer with four hidden units, and a unipolar activation function (i.e., the step function). Answer the questions below.

<ol>

 <li>For each hidden unit, analyically derive the set of inequalities based on which a set of weights and an activation threshold can be selected.</li>

 <li>Choose a particular weight vector (including the bias term), and show that the designed network achieves 100% performance in implementing the desired logic.</li>

 <li>Now assume that the input data samples are subject to small random fluctuations due to noise. Will the network you designed in <strong>part a </strong>function robustly under noisy conditions? Find the set of weights and the activation threshold for the most robust decision boundary.</li>

 <li>Generate 100 input samples by first concatenating 25 samples from each input vector. Generate a random noise vector of length 2 for each training sample, assuming a zeromean Gaussian distribution with an std of 0.2. Form validation samples for testing the NNs by linearly superposing the input samples and the random noise samples. Evaluate the classification performance (i.e., percentage correct) of the networks designed in <strong>parts a and c </strong>on the validation samples. Interpret your results.</li>

</ol>

<h1>Question 3</h1>

A researcher would like to process images of alphabet letters with a perceptron. A collection of images were compiled for training and testing the perceptron. The file assign1_data1.mat contains variables trainims (training images) and testims (testing images) along with the ground truth labels in trainlbls and testlbls. Answer the questions below.

<ol>

 <li>Visualize a sample image for each class. Find correlation coefficients between pairs of sample images that you have selected. Display the correlations in matrix format. Discuss the degree of within-class versus across-class variability.</li>

 <li>Design a single-layer perceptron with an output neuron for each digit, using the training data. Set the initial network weights <em>w </em>and bias term <em>b </em>as random numbers drawn from a Gaussian distribution N(0<em>,</em>0<em>.</em>01), assume a sigmoid activation function. Your implementation should not train each output neuron separately, but a compound matrix <em>W </em>and a compound vecor <em>b </em>should be defined and used to simultaneously update all connections. The online training algorithm should perform 10000 iterations. At each iteration, a sample image should be randomly selected from the training data, the network should be updated according to the gradient-descent learning rule, and <em>W</em>, <em>b</em>, and the mean-squared error (MSE) should be recorded. Tune the learning rate <em>η</em><sup>∗ </sup>in order to minimize the final value of the MSE. Display the final network weights for each digit as a separate image, and describe the visual characteristics.</li>

 <li>Now separately repeat the training process using a substantially higher and a subtantially lower value thant <em>η</em><sup>∗</sup>. On a single figure, plot the MSE curves (across all 10000 iterations) for <em>η<sub>high</sub></em>, <em>η<sub>low </sub></em>and <em>η</em>∗. Discuss your results.</li>

 <li>Validate the performance of the trained networks using all samples in the test data. Report the performance values for the three networks with <em>η<sub>high</sub></em>, <em>η<sub>low </sub></em>and <em>η</em>∗.</li>

</ol>