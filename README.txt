README

## Directory Structure
.
├── William_LaCroix_7038732_Assignment_2.ipynb
├── README.txt
└── eval_utf8.py


## Versions
Python: 3.8.8
NLTK: 3.6.5
Matplotlib: v3.3.4


## Runtime
The only cell which runs longer than 15s is running the Viterbi algorithm on the untagged training data (cell "Setting parameters for running Viterbi on corpus"),
which takes about 25s. This is about 14x the runtime of running the Viterbi algorithm on the untagged test data, which is about 1/16th the size of the training corpus,
so these results are not only unsurprising, but also help to reinforce our hypothesis of speed vs sentence length increasing with O(T*N^2) (see additional features for more discussion)

## Additional Features
Since runtime was a major issue for me in assignment 1, I thought it would be most interesting to extend assignment 2 by plotting the speed vs sentence length curves for running
the Viterbi algorithm on our corpora. For that purpose, I ran a timer over the call to the algorithm for each sentence in the the corpus, and plotted the graph of those data after
evaluating the accuracy of the predictions. (cells "Speed vs Sentence Length for training corpus" and "Speed vs Sentence Length for test corpus"

## Note
I had to modify the following lines from eval.py in order for the evaluator to handle the German text input:

file_gold = open(sys.argv[1], 'r', ***encoding = 'utf-8'***)
file_system = open(sys.argv[2], 'r', ***encoding = 'utf-8'***)

Thanks again, and please have yourself a damn fine day!
	~ Wilhelm