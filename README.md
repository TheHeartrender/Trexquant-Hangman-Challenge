# Trexquant-Hangman-Challenge

Problem: Trexquant Hangman Challenge

Strategy employed: Bi-LSTM with Masked Letters

Motivation: Bi-LSTM can read context from both ends of revealed string and this makes it better suited than LSTM, which reads one-way. Using masked letters 
	    for training makes sense since that is precisely the job of the code, to predict missing letters given some revealed pattern. Since this is a 
	    game, using reinforcement learning would have been good too, but, I did not use it because I already had a training dataset, and did not have 
	    time to train the model, long enough for it to develop its own optimal strategy. However, I believe, this will not be a setback, since the 
	    training is on a diverse dataset.

Description of strategy used: Instead of using sequences to train the model, I have created training data by masking random letters from the word, for each 
			      word taken from the training dataset provided for the challenge. I have used bi-LSTM which can work on the letters revealed 
			      from both sides, beginning or the end. This makes the training and prediction robust. 
			      I have obtained an accuracy of __% (reported after playing 1000 hangman games with the Trexquant Hangman API server).
