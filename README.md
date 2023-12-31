# Language-Modelling
implemented Markov models from scratch on three real world datasets.  

#### Part 1. Language Modelling.  
Created n-gram language models on different domains.  
The datasets include TED Talks, Reddit, and News domain. There are two training files:  
• ted.txt  
• reddit.txt  
And three testing files:  
• test.ted.txt  
• test.reddit.txt • test.news.txt  
  
1. Used ted.txt to create a 1-gram language model:  
   • Used both uniform probability and relative frequencies as probability to compare issues.  
   • Calculated the perplexity score for the files test.reddit.txt test.ted.txt, and test.news.txt using both models.  
2. Create n-gram language models for files ted.txt and reddit.txt with n ranging from 2 to 7.  
   • Used relative frequencies with Laplace smoothing (λ = 1).  
   • Apply each language model on the three test files (test.reddit.txt test.ted.txt, and test.news.txt) and plot the perplexity scores.
  
#### Part 2. Word Generation.  
Generated two 500 word documents (ted.out and reddit.out) using the language models which gives the lowest perplexity on the in-domain test.  

NOTE: The perplexities are very high and the word generation wouldn't make sense, the purpose of this repo is to undertand the math behind markov models as naive language models and different approaches using them.
