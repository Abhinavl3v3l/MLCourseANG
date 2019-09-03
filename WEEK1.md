# WEEK 1

#### 	1. Introduction 

1. **Machine Learning Intro**

   - Machine Learning from data.
   - Giving a machine the ability to learn a particular task by feeding it data related to task
   - With the expectation that machine can do a similar task giving it a new similar data
   - A machines ability to performs a task T gaining experience E  with respect to performance P
   - A machines ability to learn a task T and is judged with respect to a performance threshold  P performing p  hence gaining experience E. If a same program can run the same task T with an performance P > p' > p then machine has learned to perform a task a little better hence gaining more experience  E
   -  A program is said to learn from experience E performing a task T with respect to a performance  measure P if its performance at task T increases with experience E.
     - T - Playing Carrom
     - E -  Experience of playing Carrom
     - P - Probability of winning at Carrom
   - Machine Learning is classified into **Supervised Learning** and **Unsupervised Learning**.
   - Examples of Machine Learning : 
     - Audio to Text
     - Video Recognition
     - Image to Text prediction
     - Driving cars
     - Playing a board game
2. **Supervised Learning** : APPROXIMATION
1. **Condition** : We have an existing dataset with output/result.
   2. **TL;DR** Data, Direct Feedback, Predict Outcome/Future.
   3. Supervised Learning follows the model  $\theta X\rightarrow Y$
   4. Where $\theta$ is a feature and $X,Y \in \real$
   5. Supervised Learning when a program is trained on a dataset in which $X$ and $Y$ are known and  $\theta$'s' are gained as  result of training. 
   6.  Dataset is usually divided into **training** and **test** data set
   7. **Training Data** : Data is trained on this data set and a learning model is achieved
   8. **Test Data** :  Model achieved is tested on this dataset to measure the performance.
   9. Output $Y$ can be continuous or discrete  value
   10. If its continuous we are trying to map output into a continuous function. For example 
       1. price of house based on input being size hence predicting price of house is function of size.
   11. Such problem are called **Regression Problems**, like  predicting their age of a person given an his image.
   12. If output value is a discrete value we can classify them easily. For example, 
       1. the possibility of  a test to be positive or negative or classifying a cancer type, a hand drawn image is one of the numbers between 0-9/ or alphabets from A-Z,etc. The above example of predicting house price can be converted to a classification problem if we bracket them into a range. 
   13. Such problem with discrete classifiable outputs are called **Classification Problems**
   
3. **Unsupervised Learning** : Description
   1. **Condition** - We have a dataset with no output/result.
   2. **TL;DR** : No Labels, No Feedback, Find Hidden Structures in Data
      1. Unsupervised learning is like having no knowledge of data, and categorizing based on different features which is common among them. Like differentiating between 2 legged and 4 legged animals. But which are different tables/chairs or a pen.
      2. Such can be done on with images, sounds, text too.
      3. 
   3. Unsupervised learning make sense of unlabeled data and group them together.
   4. 

#### 2. Model and Cost Function

1. Model Representation
2. Cost Function
   1. Intuition I
   2. Intuition II

#### 3. Parameter Learning

1. Gradient Descent
   1. Intuition I
   2. For Linear Regression

#### 4. Linear Algebra Review

1. Matrices and Vectors
2. Addition and Scalar Multiplication
3. Matrix Vector Multiplication
4. Matrix Matrix Multiplication
5. Matrix Multiplication Properties
6. Inverse and Transpose