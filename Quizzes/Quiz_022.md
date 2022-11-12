## Quiz 22 - 
#### Program code
Create a program that produces n random values from the equation where m and s are the other inputs of the function

```.py
import random
random.seed(1234)

def produce(n, m, s):
    print("|      x       |    y(x)    |")
    print("- " * 15)
    for i in range(n):
        x = random.randint(0,100)
        y = round(x ** (1/2 * (m/s) ** 2), 2)
        x = str(x).center(10)
        y = str (y).center(10)
        print(f"|  {x}  | {y} |")
    return produce

table = produce(n = 5, m = 3, s = 2)
print (table)
```

#### Figure 1: Proof of program
<img width="372" alt="Screen Shot 2022-11-09 at 8 19 58" src="https://user-images.githubusercontent.com/105724334/200697055-93f2dffc-a506-4088-b778-6e702012433c.png">

#### Prove that A (A + B) = A
#### Figure 2: Proof of equation 
