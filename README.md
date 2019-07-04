In this project, the aim is to create a Bi-gram
HMM Part-of-Speech tagger. With this tagger we tried to tag
the words in a given test set. Language Models are insufficient
to capture the syntactic relations between the words. So with
the concept of the PoS taggers we are able to define some
syntactic rules. As like the other PoS taggers, our programs
takes some sentences from a test set and generates the tags
for the corresponding words in that sentence. This project
consist of 3 parts mainly. For the first part, creating the probabilities for the HMM model. I took the 70
percent of the set as training and 30 percent of the set. 
The second part is to execute the Viterbi
Algorithm on the test set. For the last part, the evaluation of
results needed to be done. 
In my opinion, the choice of smoothing algorithms is the
breaking point for this program. Because most of the cases, the
given data won’t be large enough to satisfy all the syntactic
conditions and that leads to the fun part for this project.
Accuracy. The first version of the solution has the
accuracy of 53 percent. Because at first i did not do any
smoothing. I was just disqualifying the sparse paths and it
lead to a horrible result. Then i tried some laplace smoothing
for the emission and transition probabilities and it did not give
satisfying results also. At the end, i have managed to increase
the accuracy to 77.61 percent by lower-casing the characters,
applying good turing smoothing, adding the transition probability for the last words(END). I have used various types of
stemmers but my accuracy decreased by 3 percent so i undo
the changes. But i mostly care about the efficiency in the program. (Avoided the repetitive code, decreased the number of
for loops, used the benefits of the dictionaries all the way, not
the repeat list and dictionary traversals and so on). Consequently i have managed to decrease the running time of my
program to min 3, max 5 seconds. (3.8 avg)
- In conclusion, i developed a PoS tagger and tried to increase the success rate of founding the given word’s tags.
