# Long Short-Term Memory

### What is LSTM?
LSTM is a type of Recurrent Neural Network which can learn and remember sequence of data. Tradition RNN lacks in remembering long context of the data which is a big issue in analysing long range of data. LSTM is a way to overcome this issue because of it's mechanism.

### Why LSTM should be used?
- Before LSTM the industry struggels to analyze long texts because traditional RRN fade away the information few steps after. LSTM handles long term dependency and it can learn from its experiances. 
- Vanishing Gradients: A problem in RNN in which  the gradient used to update teh neural network become very small. in simple terms RNN lacks to remember long term dependencies because when the data increases the neural network starts to forgot previous contexts which leads to incorrect response. 

### How LSTM works?
LSTM architecture consists one memory cell and three gates:
1. Cell State: It is used as a conveyor belt because it carries the information across time steps without doing changes in the data.
2. Forgot Gate: Forgot gate ensure to discard irrelevent information from the momory based on the relevence where the information tends to 0(less relevent) and 1(most relevent). 
3. Input Gate: Input gate is used to deside that what information is added to the memory and to prevent the memory from being overloaded.
4. Output Gate: The output gate determines what information should be used to generate the response of AI to ensure that only the necessarry and relevent information is used to genetate the response. 

### Where LSTM is used:
LSTM is used in many real world applications like :
- Speech Recognition and Virtual Assistant
- Language Translation
- Predict and Autocorrect text: 
- Time Series Forecasting: it is a static method which uses historical data to make predictions.

### Challenges for LSTM:
- Very long term dependencies: Even though LSTM is used for long term dependencies but it is also lacks in rememberig if the data is too much.
- Computer Complexity: LSTM required more computetional power than traditional RNN due to its advanced memory mechanism.
- Transformers: Transformer takes the place of LSTM in term of remembering long term dependencies because of their self attention mechanism which allows the model to process entire sequence rather than step by step.