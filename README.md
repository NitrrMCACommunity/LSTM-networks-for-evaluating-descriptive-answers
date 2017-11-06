This project aims to automatically evaluate descriptive short answers. In simple words, given a student
answer,the system compares this with faculty given modal answer and assigns numerical score to it. This is
an application of finding textual similarity between two pair of documents, where each answer can be 
treated as an individual document. 
Going through the literature review, Siamese architecture appears to be the most suitable neural network 
architecture available for finding similarity score between pair of sentences/documents.
 Each of the left and right networks is a simple two layer model:
Layer 1: a word2vec embedding is obtained for each word in the student/faculty answer
Layer 2: an lstm layer is defined on top of this word2vec embedding

The lstm layers for the left and right networks are merged together using sigmoid function to
compute similarity between answers.