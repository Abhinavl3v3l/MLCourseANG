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
1. **Condition** : We have an existing data-set with output/result.
   2. **TL;DR** Data, Direct Feedback, Predict Outcome/Future.
   3. Supervised Learning follows the model  $\theta X\rightarrow Y$
   4. Where $\theta$ is a feature and $X,Y \in \real$
   5. Supervised Learning when a program is trained on a data-set in which $X$ and $Y$ are known and  $\theta$'s' are gained as  result of training. 
   6.  Data-set is usually divided into **training** and **test** data set
   7. **Training Data** : Data is trained on this data set and a learning model is achieved
   8. **Test Data** :  Model achieved is tested on this data-set to measure the performance.
   9. Output $Y$ can be continuous or discrete  value
   10. If its continuous we are trying to map output into a continuous function. For example 
       1. price of house based on input being size hence predicting price of house is function of size.
   11. Such problem are called **Regression Problems**, like  predicting their age of a person given an his image.
   12. If output value is a discrete value we can classify them easily. For example, 
       1. the possibility of  a test to be positive or negative or classifying a cancer type, a hand drawn image is one of the numbers between 0-9/ or alphabets from A-Z,etc. The above example of predicting house price can be converted to a classification problem if we bracket them into a range. 
   13. Such problem with discrete classifiable outputs are called **Classification Problems**
   
3. **Unsupervised Learning** : Description
   1. **Condition** - We have a data-set with no output/result.
   2. **TL;DR** : No Labels, No Feedback, Find Hidden Structures in Data
      1. Unsupervised learning is like having no knowledge of data, and categorising based on different features which is common among them. Like differentiating between 2 legged and 4 legged animals. But which are different tables/chairs or a pen.
      2. Such can be done on with images, sounds, text too.
      3. 
   3. Unsupervised learning make sense of unlabelled data and group them together.

#### 2. Model and Cost Function - Supervised Learning

1. **Model Representation**

   1. Input
   $$
   x^i \in X | i = 1...m
   $$
   2. Output  
      $$
      y^i \in Y | i= 1...m
      $$
      
   3. Where $X,Y \in \real$ .
      
   4. Training Set
      $$
      (x^i, y^i) | i =1...m
      $$

   5. Given a Training set , learn a function $h: X \rightarrow Y$ so that $h(x)$ is a good predictor of $y$

   6. **End goal** : ==**a function which can predict**==.

3. **Cost Function** -  
   
   1. A $h_\theta$/function has variables : features$(\theta)$ and input data variables$(x^i)$ 
   
      2. Random features are usually assigned, data variables from data-set are constant.
      2. Function is modeled as the features are altered. Features are altered to increase accuracy using a feedback system. A feed back system can help direct the function to right direction.
   
   2. Accuracy of $h_\theta$/function is  measured using a **cost function**. 
   
      1. A cost function estimates by how far is the function from the expected output.
      2. Cost function : Its absolute difference between the predicted out $h_\theta(x)$ and output $(y)$.
      3. 
   
   3. **Idea** - **A feedback system that measure how well our hypothesis/function fits into data**
   
   4. Cost Function or Squared error function or Mean Squared Function - 
      $$
      J(\theta) = \frac{1}{2m}\sum_{i=1}^m  (h_\theta(x)-y)^2
      $$
      
   5. A visual representation
   
       ![Imagine x and y](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/_B8TJZtREea33w76dwnDIg_3e3d4433e32478f8df446d0b6da26c27_Screenshot-2016-10-26-00.57.56.png?expiry=1567641600000&hmac=xkJZfIeOCAKVNKYZqTCtNnwm9_iHKLHXrkCd-_Q7SeM)
   
   6. Altering $\theta$ 
   
      ![Variable $\theta$](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/8guexptSEeanbxIMvDC87g_3d86874dfd37b8e3c53c9f6cfa94676c_Screenshot-2016-10-26-01.03.07.png?expiry=1567641600000&hmac=8MP1j8ECYM9eq2DxmO9KUEiDmis-aHLBAjl4AstUGPQ)
   
   7. Finding the minimum $\theta$
   
      ![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/fph0S5tTEeajtg5TyD0vYA_9b28bdfeb34b2d4914d0b64903735cf1_Screenshot-2016-10-26-01.09.05.png?expiry=1567641600000&hmac=0uBP3Q0Vy71-BTMuy-yDqhDjvHKQAam17IWRf1Dg9sc)ma
   
   8. Table below represents the 
      
   | **$\theta_1$** | **$x^i$** | **$h_\theta(x^i)$** | **$J(\theta)_1​**$ |
   | -------------- | --------- | ------------------- | ----------------- |
   | 0              | 1,2,3     | 0.5,1,1.5           | 0.5               |
   | 1              | 1,2,3     | 1,2,3               | 0                 |
   | 2              | 1,2,3     | 2,4,6               | 1                 |
   
   ​    
   
   10. 
       
       
   

#### 3. Parameter Learning

1. Gradient Descent - **Estimate $\theta$ such that $h_\theta(x)$ is close to $y$**

   1. Usually gradient descent starts from a random $\theta$ values. Cost function calculates its place from the expected output. 
   2. At this point we need to minimize difference between $h_\theta(x^i)$ and $y^i$
   3. Only way to do is to change the $\theta$ values. Gradient Descent helps decide this value.

2. Objective : Find the steepest descent.(Optimization Problem)

3. [Slope Concept]: https://www.mathplanet.com/education/pre-algebra/graphing-and-functions/the-slope-of-a-linear-function	"Slope Concept"

   - First Derivative of a function will give Slope of that function- Positive or Negative	
     - Positive Slope  : left to right descent OR  If *f '*(*x*) < 0 ; then *f*(*x*) is decreasing.
     - Negative slope : right to left descent, OR  If *f '*(*x*) > 0 ; then *f*(*x*) is increasing.
     - If *f '*(*x*) = 0 ; then *f*(*x*) is at a relative maximum or minimum.

4. Gradient Descent : 

5. Partial Derivative $\frac{\part}{\part \theta}$ : Find the slope of a function , hence the direction towards the steepest descent.

6. $\alpha$ : The step/jump to take towards the direction of descent is decided  by learning rate $(\alpha)$ 

   ![Gradient Descent](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/bn9SyaDIEeav5QpTGIv-Pg_0d06dca3d225f3de8b5a4a7e92254153_Screenshot-2016-11-01-23.48.26.png?expiry=1567728000000&hmac=OIGD1Z3ocfo90QKsjTp5kxQHXaBAcYfkzHxNaw89bzM)

7. Each step down and its relative jump is relative to $\alpha$ .

8. Gradient descent algorithm is 

   1. Repeat until Convergence: 

      
      $$
      \theta_j := \theta_j - \alpha \frac{\part}{\part \theta_j}J(\theta_0,\theta_1)
      $$
      

9. Hence for function 
   $$
   h_\theta(x) = \theta_0 +\theta_1x
   $$
   Gradient Descent would algorithm would be 
   $$
   \theta_0 := \theta_0 - \alpha \frac{\part}{\part\theta_0}J(\theta_0,\theta_1)
   $$

   $$
   \theta_1 := \theta_1 - \alpha \frac{\part}{\part\theta_1}J(\theta_0,\theta_1)
   $$

    Expanding
   $$
   \theta_0 := \theta_0 - \alpha \frac{\part}{\part\theta_0}(\frac{1}{2m}\sum_{i=1}^m  ((\theta_0 +\theta_1x^{(1)})-y)^2)
   $$

   $$
   \theta_1 := \theta_1 - \alpha \frac{\part}{\part\theta_1}\frac{1}{2m}\sum_{i=1}^m  ((\theta_0 +\theta_1x^{(1)})-y)^2)
   $$

   Applying partial derivative
   $$
   \theta_0 := \theta_0 - \frac{\alpha}{m}\sum_{i=1}^m  (\theta_0 +\theta_1 x^{(1)} -y)
   $$

   $$
   \theta_1 := \theta_1 - \frac{\alpha}{m}\sum_{i=1}^m  (\theta_0 +\theta_1 x^{(1)} -y) x^{(1)}
   $$

   
