# Fake_News_Classifier
As a fun project for applying some knowledge of text data pre processing and LSTM layers.


[Dataset used can be downloaded from here](https://drive.google.com/file/d/1XQGwNIaOK-kgp8Qz0SVsZih9436ogGUm/view?usp=sharing)


# Brief explanation of pre-processing of text data--

1.All the characters apart from alphabetical english characters are replaced by space as they do not carry much linguistic information.

2.Stemming of words- All words in the corpus are reduced to their root words like "wash" for "washing","washed" etc  or "cool" for "cooling" or "cold". For classification of authentication of news root information is sufficient.

3.All alphabets are converted to their lowercases.

# Representation of words in one-hot form and then in word embeddings.

Word embeddings carries info about relative meaning of words , the features of these embedding vectors carry a semantic significance.Each word is represented as n dimensional vector where each component of it has some linguistic context.

# Model used for prediction-

As text data is a sequence data ,sequential models are required which takes into account the relevant info from previous words encountered in the text. For understanding a sentence we need to remember previous part of it too.

Bidirectional lstm is used for getting a output vector that takes into account the sequence and memory units store and forget the relevant information. Updation of any important info is done through all the units.

Then a dense layer is added that converts this output vectors from lstm layer to a single output with sigmoid function keeping value between 0 an 1 .Above 0.5 probability of being one is categoroised as 1.


During training -Adam optimiser is useed and dropout layer is also used for preventing any overfitting.<img width="1440" alt="Screenshot 2021-07-17 at 6 44 48 PM" src="https://user-images.githubusercontent.com/74730233/126038157-af75e974-0463-45db-a7bf-03f418953f1e.png">






