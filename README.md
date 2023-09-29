# Language-Modelling
implemented Markov models from scratch on three real world datasets.  

Part 1. Language Modelling  
Details: The task is to create an n-gram language model on different domains.  
The datasets include TED Talks, Reddit, and News domain. There are two training files:  
• ted.txt  
• reddit.txt  
And three testing files:  
• test.ted.txt  
• test.reddit.txt • test.news.txt  
  
1. Use the ted.txt to create a 1-gram language model:
  • Used both uniform probability and relative frequencies as probability to compare issues.
  • Calculated the perplexity score for the files test.reddit.txt test.ted.txt, and test.news.txt using both models.  
3. Use the ted.txt to create a 1-gram language model using relative frequencies as probability and Calculate the perplexity score for the files test.reddit.txt test.ted.txt, and test.news.txt.  
4. Create n-gram language models using relative frequencies for files ted.txt and reddit.txt with n ranging from 1 to 7.  
   • Apply each language model on the three test files (test.reddit.txt test.ted.txt, and test.news.txt) and plot the perplexity scores.  
5. Create two an n-gram language models using relative frequencies for files ted.txt and reddit.txt with Laplace smoothing (λ = 1). Use values of n from 2 to 7. Apply each language model on the three test files (test.reddit.txt test.ted.txt, and test.news.txt) and plot the perplexity scores.
Part 3. [10 pts] Generate two 500 word documents (ted.out and reddit.out) using the language models which gives the lowest perplexity on the in-domain test.
For example, if 4-gram language model gave the lowest perplexity for ted.txt and 5-gram for reddit.txt, then use 4-gram ted talk language model to generate the ted.out file and 5-gram reddit language model to generate reddit.out file. Compute the perplexity of the text for each.
Creating a Language Model
Given a sequence ‘this is a sentence .’ language models (LM) can be calculated as follows.
Unigram LM
Probability of the sentence is the product of relative frequencies of each word.
P (this, is, a, sentence, .) ≈ Pr (this)Pr (is)Pr (a)Pr (sentence)Pr (.) Here Pr(wi) = Frequency of word wi
Total frequency of all the words
Bigram LM
P (this, is, a, sentence, .) ≈ Pr (this)Pr (is|this)Pr (a|is)Pr (sentence|a)Pr (.|sentence) Here Pr(wi|wi−1) = Frequency of words wi and wi−1 occurring together
Total frequency of word wi−1
Trigram LM
P (this, is, a, sentence, .) ≈ Pr (this)Pr (is|this)Pr (a|this, is)Pr (sentence|a, is)Pr (.|sentence, a) Here Pr(wi|wi−1,wi−2) = Frequency of words wi,wi−1 and wi−2 occurring together
Total frequency of word wi−1 and wi−2 occurring together
2
   
n-gram LM
n=N n=N P(this,is,a,sentence,.) ≈ Y Pr(wi|wi−1,··· ,wi−(n−1)) = Y Pr(wi|history)
i=1 i=1
Here Pr(wi|history) = Frequency of word wi occurring together with history
Total frequency of history
Calculating Perplexity
Perplexityofasequencew1,w2,···,wN is:
PPL = P(w1,w2,··· ,wN)−N1
=Ns 1 P(w1,w2,··· ,wN)
Here P (w1 , w2 , · · · , wN ) is the probability for the sequence calculated using the specific language model.
The smaller the perplexity value, the better the language model.
Generating Text
To generate text, use the specific language model and pick the highest proba- bility word given the previous predictions.
To generate the first word, pick the word with the highest probability no
argmax P(wi) wi
To generate any word, pick the word with the highest probability given the previous n − 1 predictions
arg max nP (wi|wi−1, · · · , wi−(n−1))o wi
Here P(·) is the probability calculated using the specific language model.
   3

Submission
This is an individual assignment. Each person should submit as a single zip file named with assignment number and the username (e.g. HW2 akhan4.zip). The zip file should contain the required code file and a readme file. The readme should include the following:
– one line descriptions of the code file
– Perplexity scores for uniform language model (part 1)
– Perplexity scores for unigram language model (part 2)
– Plot for ted talk and reddit n-gram language models without smoothing (part 3)
– Plots for ted talk and reddit n-gram language models with laplace smooth- ing (part 4)
– Perplexity scores for the two word documents (part 5)
Remember that after general discussions with others, you are re- quired to work out the problems by yourself. All submitted work must be your own, though you can get help with others, so long as you cite the help. Please refer to the Stevens Honor System for clarifications.
4

