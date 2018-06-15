---
layout: post
title: XOR Introduction to Neural Networks - Part 1
---
### The basics of neural networks
Traditionally, programs need to be hard coded with whatever you want it to do. If they are programmed using extensive techniques and painstakingly adjusted, they may be able to cover for a majority of situations, or at least enough to complete the necessary tasks. However, ***neural networks*** are a type of algorithm that's capable of learning. Well, kinda. Let me explain..

Neural networks are a type of program that are based on, very loosely, a human neuron. All you really need to know about a neuron, without turning this into a bio lesson, is that there is an <u>input area</u>, a processing area in that carries information which connects the output of one neuron to the input of another - known as <u>synapses</u> - and an <u>output</u> area. These branch off and connect with many other neurons, passing information from the brain and back. Millions of these neural connections exist throughout our bodies, collectively referred to as ***neural networks***.

<center> <img src="/images/neuron.gif" alt="Human Neuron Gif"/> </center>


Now that we've discussed real neural networks, we can start looking at ***artificial neural networks***. Like the biological kind, an artificial neural network has <u>inputs</u>, a <u>processing area</u> that transmits information, and <u>outputs</u>. However, these are much simpler, in both design and in function, and nowhere near as powerful as the real kind.

Here is a diagram of a basic artificial neuron:

<img src="/images/basicNN.png" alt="Basic Neuron"/>

This is an example of a simple 3-input, 1-output neural network. As we talked about, each of the neurons has an input, I<sub><i>n</i></sub>, a connection to the next neuron layer, called a ***synapse***, which carries a weight W<sub><i>n</i></sub>, and an output layer. In this case, there is only one output.

The easiest way to understand what's taking place is to think of it like this: by multiplying two numbers together, you can theoretically get any number.

The two numbers in this case are the input and the synaptic weight. The number we are trying to get is the output.
Since the starting synaptic weight is random, it is highly likely the network will need to do some adjusting, or as I like to call it, learning, before it reaches the correct output.

The basic idea is to take the input, multiply it by the synaptic weight, and check if the output is correct. If it is not, adjust the weight, multiply it by the input again, check the output and repeat, until we have reached an ideal synaptic weight.

### What is XOR?
-------------------------------
An XOR gate is a kind of logic gate. It is a very simple example of a specific combination of inputs causing an output. Here it is below, we won't get into too many details as you really only need to know the way it works.

|Input 1   |Input 2   ||Output|
|:--------:|:--------:||:-----:|
| 0        | 0        || OFF|
| 0        | 1        || ON |
| 1        | 0        || ON |
| 1        | 1        || OFF |

The pattern here is that if both inputs are the same, the output is off, and if both inputs are different, the output is on.

### Getting into the details
--------------------------------------
Let's look at it using some raw numbers.

Remember how I said the main idea is that you want to multiply the inputs by the right numbers to get the output?

We'll give our inputs, which is either 0 or 1, and they both will be multiplied by the synaptic weight. We'll adjust it until we get an accurate output each time, and we're confident the neural network has learned the pattern.

In order to do that, all elements have to be numbers. So we'll assign a number to each output, 0 for off, 1 for on. (This is called ***classification***, or specifically, ***binary classification***, but more on that in another post).

So to write this out in math terms, it's the sum of all the inputs multiplied by their synaptic weights. Here's the equation:

<center> <img src="/images/derive-equation.png" alt="inputs x weights" height=100/> </center>

Which is, in broader terms:

<center> <img src="/images/equation.png" alt="inputs x weights" height=100/> </center>

The outputs can also be represented as the dot product of the inputs and the synaptic weights:

<center> <img src="/images/messymatrix.png" alt="matrix of inputs x weights" height=100/> </center>

