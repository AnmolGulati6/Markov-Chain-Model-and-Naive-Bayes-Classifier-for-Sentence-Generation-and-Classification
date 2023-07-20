# Markov Chain Text Generation and Naive Bayes Classifier for Movie Script Analysis

### Introduction
This project, done as part of the CS-540 Intro to AI course at UW Madison. In this project, I have implemented a Markov chain text generation model based on a movie script. The script used for this project is "Joker," which was obtained from IMSDb (The Internet Movie Script Database). The objective is to generate new sentences that may contain sensible words and phrases using the Markov chain model. Additionally, a Naive Bayes classifier is built to distinguish sentences from the original script and sentences from a fake script.

### Part 1: Markov Chain Text Generation
1. **Data Preprocessing:** The script is converted to lowercase, and all non-letter characters are removed. Consecutive spaces are replaced with a single space to ensure there are no consecutive spaces.

2. **Bigram Transition Probability Table:** A 27x27 matrix is constructed to represent the bigram character transition probabilities, with "space" followed by the letters "a" to "z."

3. **Trigram Transition Probability Table:** Although not submitted, a 27x27x27 array or a 729x27 matrix is constructed to represent the trigram transition probabilities. 

4. **Sentence Generation:** Using the trigram model, 26 sentences, each containing 1000 characters, are generated. The bigram model is utilized to generate the second character, and in cases where the current two-character sequence never appeared in the script, the bigram model is switched for probabilities calculation. The sentences produced are shared in the output.

### Part 2: Naive Bayes Classifier
1. **Data Preprocessing:** The fake script is obtained and preprocessed similarly to the original script.

2. **Unigram Transition Probability Table:** Unigram probabilities are computed for both the original and fake scripts.

3. **Likelihood Probabilities:** Likelihood probabilities of the Naive Bayes estimator for the fake script are computed using the unigram probabilities.

4. **Posterior Probabilities:** Posterior probabilities of the Naive Bayes estimator for the fake script are calculated based on the prior probabilities (Pr{Document = your script} = 0.77 and Pr{Document = fake script} = 0.23) and the likelihood probabilities.

5. **Classification:** Using the Naive Bayes model, the 26 sentences generated in Part 1 are classified as either belonging to the original script or the fake script. The classification results are written to a file named `classification.txt`.

### Running the Code
To run the code and generate the results, make sure you have the script file named `script.txt` and the fake script file named `fake_script.txt` in the same directory as the Python script. Also, ensure that the required libraries (numpy) are installed.

Simply run the Python script, and it will execute the Markov chain text generation and Naive Bayes classifier tasks, generating sentences, and classifying them accordingly.

Feel free to explore the generated sentences and experiment with different movie scripts to observe how the model performs.

Enjoy the Markov chain text generation and Naive Bayes classification!

*Written by Anmol Gulati*
