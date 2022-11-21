## Quiz 21 
#### Program code
Using the function that produces the table of Truth for 3 inputs, add a column for the boolean equation.

```.py
def get_truth ():
    print ("|    C     |    B     |    A     | AB + not B + not CB |")
    print ("- " * 28)

    for x in range (8):
        a = x // 4
        b = (x % 4) // 2
        c = x % 2
        d = int(a and b) or int(not b) or int(not b and c)
        a = str(a).center(10)
        b = str(b).center(10)
        c = str(c).center(10)
        d = str(d).center(21)
        print (f"|{a}|{b}|{c}|{d}|")

table = get_truth()
print (table)
```

#### Figure 1: Proof of program
<img width="570" alt="Screen Shot 2022-11-09 at 8 14 40" src="https://user-images.githubusercontent.com/105724334/200696341-aef8910f-32b1-4675-b9e7-f75a2d557aa3.png">

#### Boolean Circuit & Truth Table 
Equation: X = ZW + (Z + Y(not W)) 
#### Figure 2: Truth Table 
![IMG_0459](https://user-images.githubusercontent.com/105724334/201460652-8e32b50b-9521-43a8-b44a-d615a8e3ee27.jpg)

#### Figure 3: Circuit 
Equation: X = ZW + (Z + Y(not W)) 
![IMG_0475](https://user-images.githubusercontent.com/105724334/202938549-6246f71a-37c1-4e0d-a1cf-2def478b2ad5.jpg)

