# MLQ1Project

Veterans Affairs WebPage Data Project Report

Statement of Data Mining Goal:

Veterans Affairs (VA) is a government agency that is supposed to process claims and provide benefits to Veterans. However, Veterans often have a very difficult time actually claiming the benefits they deserve, because the process to go through the VA can be difficult and tedious. The goal of research in this area is to help Veterans with the process of filing for claims. This projects specific goal is to evaluate the quality of embeddings of the datascraped text.

Description of Dataset:

Data was collected from this website: www.knowva.ebenefits.va.gov, a publicly accessible government website about the rules and regulations behind filing for claims with the Veterans. In the website, theres thousands of article webpages that contain these rules. We created our dataset by extracting the text from each of these pages. Each of these articles is also associated with a broader category.


Preprocessing:

The text from these pages was broken into appropriately sized chunks, if the text in an article was over 500 words. Then, each chunk of text was fed through an openAI embedding model to create embeddings for each chunk of text. Duplicate texts were removed, and special non-recognized characters were also deleted.


(Non-Weka) No Attribute Removal
As a baseline method, we keep all the attributes in our data. This is also helpful as a control case to help us put into perspective the other results of our trials. 
PrincipalComponents 
PCA (Principal Component Analysis) is a attribute reduction technique that transforms the original attributes into a linear combination of attributes called Principal Components that tries to maximize the variance in the data. The PCA ranks n (# of original attributes) principal components by the amount of variance they capture. By keeping a variance threshold, we can remove some attributes which do not contain enough variance for our liking.
ReliefFAttributeEval 
ReliefF attribute evaluation is an attribute selection algorithm that ranks the attributes by useful they are in distinguishing between the class types.
ReliefF is effective for handling noisy data since it focuses on the nearest neighbors, which is helpful for our data. 
ReliefF attribute evaluation finds the similarities between different instances and the give a weight for each attribute in relation to the class .
GainRatioAttributeEval 
GainRatioAttribute Eval ranks attributes by their gain ratio in relation to the class attribute. Entropy is calculated by the following formula where P(Ci) is the probability of the attribute predicting the class.  
Correlation
Correlation ranks attributes based on their correlation to each potential output class, and the attributes that have the highest correlation to one or more output classes are chosen

Classification Algorithms:

Multi-Layer Perceptron
Partial Decision Tree
Naive Bayes
J48
