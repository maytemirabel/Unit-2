## Quiz 23
#### Program code
Create a program that produces the graph for the function in Quiz #22  

```.py
from matplotlib import pyplot as plt
import random
random.seed(1234)

def produce(n, m, s):
    print("|    x     |   y(x)   |")
    print("- " * 12)
    x_list = []
    y_list = []
    for i in range(n):
        x = random.randint(0,100)
        x_list.append(x)
        y = round(x ** ( 1 / 2 * (m / s) ** 2),2)
        y_list.append(y)
        x = str(x).center(10)
        y = str(y).center(10)
        print(f"|{x}|{y}|")
    return y_list,x_list

data_x, data_y = produce(n = 5, m = 3, s = 2)
plt.plot(data_x, data_y)
plt.xlabel("x")
plt.ylabel("$y = x^{1/2*(m/s)^2}$")
plt.show()
```

#### Figure 1: Proof of program
<img width="409" alt="Screen Shot 2022-11-13 at 13 58 07" src="https://user-images.githubusercontent.com/105724334/201506566-fd5df8bd-af8c-4fc2-9b0c-5aa46782cb1b.png">

#### Figure 2: Graph for function
<img width="644" alt="Screen Shot 2022-11-13 at 13 58 23" src="https://user-images.githubusercontent.com/105724334/201506569-3304cd7c-a1c5-4dda-a2d8-a347d802cb12.png">

#### Truth Table 
Equation: A(A+B) 
#### Figure 3: Truth Table
![IMG_0464](https://user-images.githubusercontent.com/105724334/201505994-5e53bdb8-d8cf-46b7-b89c-5e406d51bfca.jpg)
