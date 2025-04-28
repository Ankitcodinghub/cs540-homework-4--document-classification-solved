# cs540-homework-4--document-classification-solved
**TO GET THIS SOLUTION VISIT:** [CS540 Homework 4- Document Classification Solved](https://www.ankitcodinghub.com/product/cs540-hw4-document-classification-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;117934&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS540 Homework 4- Document Classification Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
Summary

In this assignment you’ll be tackling the problem of document classification. You are given the skeleton code classify.py, and you will need to implement the functions as required.

Document Classification

We’ll be reading in a corpus (a collection of documents) with two possible labels and training a classifier to determine which label a query document is more likely to have.

You will need: hw4.zip, which includes 2 directories: corpus and EasyFiles.

For this program, you must write the following seven (7) Python functions: train(training_directory, cutoff) — load the training data, estimate the prior distribution P(label) and class conditional distributions , return the trained model

create_vocabulary(directory, cutoff) — create and return a vocabulary as a list of word types with counts &gt;= cutoff in the training directory create_bow(vocab, filepath) — create and return a bag of words Python dictionary from a single document

load_training_data(vocab, directory) — create and return training set (bag of words Python dictionary + label) from the files in a training directory

prior(training_data, label_list) — given a training set, estimate and return the prior probability

P(label) of each label

p_word_given_label(vocab, training_data, label) — given a training set and a vocabulary, estimate and return the class conditional distribution over all words for the given label using smoothing

classify(model, filepath) — given a trained model, predict the label for the test document (see below for implementation details including the return value) this high-level function should also use create_bow(vocab, filepath)

You are allowed to write additional helper functions. Your submitted code should not produce any additional printed output.

Toy Example

Create Vocabulary

To create the vocabulary for your classifier, traverse BOTH of these subdirectories under train/ (note: do not include test/) and count the number of times a word type appears in any file in either directory.

As a design choice, we will exclude any word types which appear at a frequency strictly less than the cutoff argument (cutoff = 1 means retain all word types you encounter). Return a sorted list of these word types.

Create Bag of Words

This function takes a path to a text file (assume a valid format, one token per line), reads the file in, creates a bag-of-words representation based on the vocabulary, and returns the bag-of-words in dictionary format. Give all counts of word types not in the vocabulary to out of vocabulary (OOV) (see below).

If you encounter a word type that does not appear in the provided vocabulary, add the non-string value None as a special key to represent OOV. Collect counts for any such OOV words.

Load Training Data

Python’s os module (https://docs.python.org/3/library/os.html) will be helpful here, particularly its listdir() function.

&gt;&gt;&gt; vocab = create_vocabulary(‘./EasyFiles/’, 1)

&gt;&gt;&gt; load_training_data(vocab,’./EasyFiles/’)

The dictionaries in this list do not need to be in any particular order. You should notice that the directory string will always include a trailing ‘/’ as shown here.

NOTE: All subsequent functions that have a training_data parameter should expect it to be in the format of the output of this function, a list of two-element dictionaries with a label and a bag-of-words.

Log Prior Probability

This method should return the log probability of the labels in the training set. In order to calculate these, you will need to count the number of documents with each label in the training data,

You are required to use add-1 smoothing (Laplace smoothing) here. Since we only have two labels here, the equation will look like:

Note that the return values are the natural log of the probability. In a Naive Bayes implementation, we must contend with the possibility of underflow: this can occur when we take the product of very small floating point values. As such, all our probabilities in this program will be log probabilities, to avoid this issue.

Log Probability of a Word, Given a Label

This function returns a dictionary consisting of the log conditional probability of all word types in a

vocabulary (plus OOV) given a particular class label, . To compute this probability, you will use add-1 smoothing to avoid zero probability. You will find this

(https://happyharrycn.github.io/CS540-Fall20/lectures/statistics_nlp.pdf) be helpful.

&gt;&gt;&gt; vocab = create_vocabulary(‘./EasyFiles/’, 1)

&gt;&gt;&gt; training_data = load_training_data(vocab, ‘./EasyFiles/’)

6, ‘a’: -3.044522437723423, ‘cat’: -3.044522437723423, ‘chases’: -3.044522437723423, ‘dog’: -3.04452243772342

71634776, ‘world’: -3.044522437723423, None: -3.044522437723423}

53358316, ‘world’: -2.3978952727983707, None: -3.091042453358316}

&gt;&gt;&gt; vocab = create_vocabulary(‘./EasyFiles/’, 2)

&gt;&gt;&gt; training_data = load_training_data(vocab, ‘./EasyFiles/’)

=&gt; {‘.’: -1.6094379124341005, ‘a’: -2.302585092994046, None: -0.35667494393873267}

=&gt; {‘.’: -1.7047480922384253, ‘a’: -1.2992829841302609, None: -0.6061358035703157}

Note: In this simple case, we have no words in our training set that are out-of-vocabulary. With the cutoff of 2 in the real set, we will see a number of words in the training set which are still out-of-vocabulary and

map to None . These counts should be used when calculating , and the existence of an “out-of-vocabulary” word type should be used when calculating all probabilities.

Train

Given the location of the training directory and a cutoff value for the training set vocabulary, use the previous set of helper functions to create the following trained model structure in a Python dictionary:

For the EasyFiles data and a cutoff of 2, this would give (formatted for readability):

&gt;&gt;&gt; train(‘./EasyFiles/’, 2)

=&gt; {‘vocabulary’: [‘.’, ‘a’],

The values for None are so high in this case because the majority of our training words are below the cutoff and are therefore out-of-vocabulary.

Classify

Given a trained model, this function will analyze a single test document and give its prediction as to the label for the document. The return value for the function must have the Python dictionary format

, where corresponds to each

(Recall: use log probabilities! When you take the log of a product, you should sum the logs of the operands.)

Deliverables

Please submit your files in a zip file named hw4_&lt;netid&gt;.zip, where you replace &lt;netid&gt; with your netID (your wisc.edu login). Inside your zip file, there should be only one file named: classify.py. Do not submit a Jupyter notebook .ipynb file.

Note:

1. The directory path will always end with a ‘/’.

2. The grading will be conducted automatically, please follow the guidelines strictly.

hw4

Criteria Ratings Pts

create_vocabulary three test cases 15.0 pts

create_bow three test cases 15.0 pts

load_train_data 10.0 pts

prior 10.0 pts

p_word_given_label 25.0 pts

train 10.0 pts

classify 15.0 pts
