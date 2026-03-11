# Fitting Poisson  distribution
# Aim : 

To fit poisson distribution for the arrival of objects per minute from the feeder

# Software required :  

Python and Visual component tool

# Theory:

The Poisson distribution is the discrete probability distribution of the number of events occurring in a given time period, given the average number of times the event occurs over that time period.

![image](https://user-images.githubusercontent.com/104613195/166248326-fd042076-8b0b-40c4-8b11-1d8e8fcb74db.png)

 Conditions for Poisson Distribution:

1. An event can occur any number of times during a time period.
2. Events occur independently. I
3. The rate of occurrence is constant.
4. The probability of an event occurring is proportional to the length of the time period. 
 
# Procedure :

![image](https://user-images.githubusercontent.com/104613195/166251988-d0c53205-6080-4f7b-ae4c-398178586637.png)

# Experiment :

![image](https://user-images.githubusercontent.com/103921593/230282876-f4a5afbf-cac1-4648-a1b0-c78840638a8e.png)

# Program :
```
# Fitting Poisson Distribution (User Input)

import math

# Number of observations
n = int(input("Enter number of observations: "))

data = []

# Getting data from user
for i in range(n):
    x = int(input("Enter number of arrivals: "))
    data.append(x)

# Calculate mean (lambda)
lam = sum(data) / len(data)
print("Mean (lambda) =", lam)

# Poisson function
def poisson(x, lam):
    p = (lam**x * math.exp(-lam)) / math.factorial(x)
    return p

# Calculate probabilities
print("\nPoisson Probabilities:")
for x in range(6):
    p = poisson(x, lam)
    print("P(X =", x, ") =", round(p,4))
```

 

# Output : 

<img width="822" height="582" alt="image" src="https://github.com/user-attachments/assets/1819da90-2bd8-4cd8-91f3-7ee6ead34137" />


# Results

The Poisson distribution is fitted for the objects arrived from feeder per minute and the data is tested using Chi-square test. 
 
