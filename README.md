# Brief Summary 
We use Python to perform Named Entity Recognition on text in order to retrieve important information from natural language. The applications of this include converting data that is unstructured to structured data. Using Tensorflow, we implement a Bidirectional Long Short Term Memory Recurrent Neural Network to recognize named entities. Using this we achieve a validation accuracy of 97%. To try it out yourself just go to the bottom and change the input string, running that cell will return your input with named entities highlighted and their type declared beside it.

<img width="1069" alt="Screenshot 2023-10-21 at 4 41 07 PM" src="https://github.com/andrew-dusa/Named-Entity-Recognition/assets/93221044/1235560f-b460-4818-b2db-db11a06663aa">

## Bidirectional Long Short Term Memory:
A BiLSTM is a type of recurrent neural network(RNN) that is used in various natural language processing(NLP) tasks. It is an extension of the tradional LSTM that processes inputs in both forward and backward directions. This allows it to capture information from past and future contexts simulaneosly. See [Google’s Neural Machine Translation System: Bridging the Gap between Human and Machine Translation](https://arxiv.org/pdf/1609.08144.pdf) to see the improved context at each point when using a bi-directional RNN for the encoder.

![Screenshot 2023-10-21 at 4 33 42 PM](https://github.com/andrew-dusa/Named-Entity-Recognition/assets/93221044/21d089ec-3956-4699-8a50-77e57c310e74)


## Here are the steps of how it works:
1. Input:
The input to a BiLSTM is a sequence of data points. It could be a sentence in natural language, or any other sequential data.
2. Forward/Backward LSTM:
The input is first passed through a forward LSTM layer that process the data from a left-to-right manner, capuring information from past to present. At the same time, the same input is also passed through a backwards LSTM layer to process the data in a right-to-left manner, capturing info from present to future.
3. Combining the Forward and Backwards Outputs:
Next the aforementioned outputs are combined at each time step, merging the information captured from both directions.
4. Output:
The merged output sequence is a combination of past and future context information for each time step in the input sequence. This output can be used for various, such as sentiment analysis, machine translation, or in this case Named Entity Recognition as we have done here.
## Benefits of using Bidirectional LSTMs
1. Contextual Understanding: BiLSTMS can capture context from both directions and can help to better undersatnd the meaning of words as presented in natural language.
2. Layer Combinations: You can stack multiple layers of BiLSTMs to capture more complex or abstract features from the input sequence.
3. Reduce Vanishing Gradient Problem: BiLSTMs mitigate the vanishing gradient problem through the use of gating mechanisms. allowing them to handle long-range dependencies effectively.
