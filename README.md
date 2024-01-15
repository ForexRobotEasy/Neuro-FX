# Neuro FX EA ReadMe

This is the ReadMe file for the Neuro FX EA, a Forex trading expert advisor. The Neuro FX EA is developed by [Forex Robot Easy Team](https://forexroboteasy.com), but please note that ForexRobotEasy is not the official developer of this product. This sample code is provided to demonstrate how the expert advisor works based on the product description found at [here](https://forexroboteasy.com/forex-robot-review/neuro-fx-review-buy-and-get-bonus-ea-for-free/). To find the official developer of this product, please refer to MQL5.

## Expert Advisor Code

The code provided here is the implementation of the Neuro FX EA expert advisor. This expert advisor is designed to trade on the EURUSD currency pair with the following parameters:

- Symbol: EURUSD
- Lot Size: 0.1
- Stop Loss: 50 pips
- Take Profit: 100 pips

### Initialization

The expert advisor initializes the necessary libraries and defines the constants for symbol, lot size, stop loss, and take profit. It also declares and initializes global variables, as well as creates instances of the CTrade and CNeuralNetwork classes.

### OnInit()

The OnInit() function is called when the expert advisor is initialized. In this function, the neural network parameters are set up using the CNeuralNetwork class. The input size is set to 2, a hidden layer with 5 neurons is added, and the output size is set to 1. The trade parameters are set up using the CTrade class, such as the symbol, volume, stop loss, and take profit.

### OnTick()

The OnTick() function is called on every tick of the market. It gets the current market price using the MarketInfo() function. If the current price is higher than the previous price, the neural network is used to make a buy decision. The previous and current prices are set as inputs to the neural network, and the Calculate() function is called to perform the calculation. The output of the neural network is obtained using the GetOutput() function. If the output is greater than 0.5, a buy trade is opened using the Buy() function.

### OnDeinit()

The OnDeinit() function is called when the expert advisor is deinitialized. It closes all open trades using the CloseAll() function of the CTrade class.

## Product Description

The Neuro FX EA is a Forex trading expert advisor that utilizes a neural network for making buy decisions. It is designed to trade on the EURUSD currency pair with a lot size of 0.1. The expert advisor sets a stop loss of 50 pips and a take profit of 100 pips for each trade.

The neural network used in this expert advisor has an input size of 2, a hidden layer with 5 neurons, and an output size of 1. It takes the previous and current market prices as inputs and calculates the output based on its internal weights and biases. If the output is greater than 0.5, a buy trade is opened.

Please note that ForexRobotEasy is not the official developer of this product. This code is only a sample implementation provided to demonstrate how the expert advisor works based on the product description. To find the official developer of this product, please refer to MQL5. For detailed reviews and trading results of this product, you can visit the [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/neuro-fx-review-buy-and-get-bonus-ea-for-free/) website.
