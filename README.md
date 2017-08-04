# Cortex.js

`Cortex.js` is a simple JavaScript libary meant to emulate a simple [neural network](http://en.wikipedia.org/wiki/Artificial_neural_network)

:bulb: **Note**: This is meant to be used in conjunction with Darwin.js. I did not create this libary to be used solely as a neural network library. It does not include any functions to train the network. Feel free to implement this yourself.

A simple example of how to use the library
The following code will create a basic network with 3 input neurons, 1 hidden layer with 4 neurons, and 2 output neurons
<img src="https://cdn-images-1.medium.com/max/1200/1*5GSpUs2hWFx4Lq2_KCyulg.png" alt="Basic neural network" width=300px/>

```javascript
let network;

network = new Perceptron();
network.activation = Cortext.activation.sigmoid(); // Any activation function can be implemented;
network.inputLayer = new Layer(3);
network.hiddenLayer = [new Layer(4)];
network.outputLayer = new Layer(2);

network.generate();
network.activate([0.5, 0.5, 0.5]); // Feed in an input

network.setWeights([0.5, 0.5, 0.5, 0.5, 0.5, 0.5...]); // Set the weights
```