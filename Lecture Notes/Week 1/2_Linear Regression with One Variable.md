# Model Representation

Notations:
* m = Number of training examples
* x's = "input" variable/features
* y's = "output" variable/"target" variable
* (x,y) = one training example
* (x<sup>i</sup>, y<sup>i</sup>) = i<sup>th</sup> training example

Training Set -> Learning Algorithm -> Hypothesis

Size of house (x) -> Hypothesis -> Estimated price (estimated value of y)

Hypothesis maps from x's to y's.

### How do we represent _h_?
Hypothesis: h<sub>Θ</sub>(x) = Θ<sub>0</sub> + Θ<sub>1</sub>x

Shorthand for h<sub>Θ</sub>(x): h(x)

Therefore, h(x) = Θ<sub>0</sub> + Θ<sub>1</sub>x

![Image of Graph](img/2_graph.png)

This model is called **linear regression with one variable** (which is x). Another name is **univeriate linear regression**. Univeriate is a fancy way of saying "one variable".

# Cost Function
This will help us figure out how to fit the best possible straight line to our data.

Θ<sub>i</sub>'s are the _parameters_ of the model.

### How to choose Θ<sub>i</sub>'s?

Review of linear regression: Different parameters will yield different results: 
![Image of different theta parameters and graphs](img/2_different_parameters.png)

Idea: Choose Θ<sub>0</sub>, Θ<sub>1</sub> so that h<sub>Θ</sub>(x) is close to y for our training examples. This is done on our training data set where we have both x and y.

**Just remember**: We want h<sub>Θ</sub>(x) - y to be small as it is the difference between our estimation (h<sub>Θ</sub>(x)) and our actual (y) outputs. 

The instructor then adds (h<sub>Θ</sub>(x) - y)<sup>2</sup> which makes the minimization become "minimize the _square_ difference between estimated and actual".

Remember that we are using this: (x<sup>i</sup>, y<sup>i</sup>) = i<sup>th</sup> training example.

With that said, we want to "sum" over our training set which looks like this:
![Image of formal minimization definition](img/2_formal_minimize.png)

Don't forget that, 
h<sub>Θ</sub>(x<sup>i</sup>) = Θ<sub>0</sub> + Θ<sub>1x</sub><sup>i</sup>

The "minimize Θ<sub>0</sub> Θ<sub>1</sub>" translates to "find me the values of Θ<sub>0</sub> and Θ<sub>1</sub> that causes h<sub>Θ</sub>(x<sup>i</sup>) = Θ<sub>0</sub> + Θ<sub>1x</sub><sup>i</sup> to be **minimized**".

### Formal definition of cost function:

![Formal definition of cost function](img/2_formal_def_cost_function.png)

This is also called the _squared error cost function_ because we are evaluating error costs by squaring the differences of expected and actual. There are other cost functions that can be used too.

# Cost Function - Intuition I

Quick recap!

**Hypothesis:**

h<sub>Θ</sub>(x) = Θ<sub>0</sub> + Θ<sub>1</sub>x

**Parameters:**

Θ<sub>0</sub>, Θ<sub>1</sub>

**Cost Function:**

![cost function](img/2_cost_function.png)

**Goal:**

Minimize J(Θ<sub>0</sub>, Θ<sub>1</sub>)

**We will use a Simplified Hypothesis!**

h<sub>Θ</sub>(x) = Θ<sub>1</sub>x

This is basically setting  Θ<sub>0</sub> = 0. 

Using this simplified hypothesis, we are choosing only hypothesis functions that pass through the origin (0,0). 

From here, I did the calculations on paper but you can see the overview of the notes [here](https://www.coursera.org/learn/machine-learning/supplement/u3qF5/cost-function-intuition-i) but here is what I got out of it: 

Essentially for different values of Θ<sub>1</sub> you can plot J(Θ<sub>1</sub>) which is our cost function. When you plot this you'll begin too see something like this:

![cost function graph](img/2_cost_function_graph.png)

Since the cost function is to minimize J(Θ<sub>1</sub>) you want to find the value of Θ<sub>1</sub> that yields the smallest ouput from J(Θ<sub>1</sub>). In this example, J(1) = 0 which is the best minimized output as you can clearly see in the graph above.

# Cost Function - Intuition II

This video section was showing how having two parameters affects what we did in the last section, where we used only one parameter.

What we see here is the use of a contour plot to visualize where the best values of Θ<sub>0</sub>, Θ<sub>1</sub> are at, in order to minimize J(Θ<sub>0</sub>, Θ<sub>1</sub>).

Here is an example where the values are very close to the minimum:

![image of contour plot](img/2_contour.png)