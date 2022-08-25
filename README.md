# Problem Statement
Suppose you are the CEO of a restaurant franchise and are considering different cities for opening a new outlet.
- You would like to expand your business to cities that may give your restaurant higher profits.
- The chain already has restaurants in various cities and you have data for profits and populations from the cities.
- You also have data on cities that are candidates for a new restaurant. 
    - For these cities, you have the city population.
    
Can you use the data to help you identify which cities may potentially give your business higher profits?

# Solution
The goal is to build a linear regression model to fit this data.
- With this model, we can then input a new city's population, and have the model estimate our restaurant's potential monthly profits for that city.

## Linear Regression Model
We will fit the linear regression parameters $(w,b)$ to our dataset.
- The model function for linear regression, which is a function that maps from `x` (city population) to `y` (restaurant's monthly profit for that city) is represented as  
        𝑓(𝑥)=𝑤𝑥+𝑏

- To train a linear regression model, we want to find the best $(w,b)$ parameters that fit our dataset.  

    - To compare how one choice of $(w,b)$ is better or worse than another choice, we can evaluate it with a cost function $J(w,b)$
      - $J$ is a function of $(w,b)$. That is, the value of the cost $J(w,b)$ depends on the value of $(w,b)$.
  
    - The choice of $(w,b)$ that fits your data the best is the one that has the smallest cost $J(w,b)$.


- To find the values $(w,b)$ that gets the smallest possible cost $J(w,b)$, you can use a method called **gradient descent**. 
  - With each step of gradient descent, your parameters $(w,b)$ come closer to the optimal values that will achieve the lowest cost $J(w,b)$.
  

- The trained linear regression model can then take the input feature $x$ (city population) and output a prediction 𝑓(𝑥) (predicted monthly profit for a restaurant in that city).
