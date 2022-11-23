## Quiz 24
#### Program code
Create a program that shows the graph of the parabola for 100 values of x in the interval of -10 to 10

Equation: $y = 2 (x + 9)^2$

```.py
from matplotlib import pyplot as plt
def produce():
    x_out = []
    y_out = []
    st = -10
    for i in range(101):
        x_out.append(st)
        y = 2 * (st + 5 )**2
        y_out.append(y)
        st += 0.2
    return x_out, y_out


data_x, data_y = produce()
plt.ylabel('$f(x) = 2(x+5)^2$')
plt.xlabel('x')
plt.plot(data_x, data_y)
plt.show()
```

#### Figure 1: Parabola of the equation 
![Screen Shot 2022-11-13 at 14 36 19](https://user-images.githubusercontent.com/105724334/201507561-802639f4-c333-41e8-b3df-2f23ad418c8a.png)

#### Boolean Circuit 
Equation: not(bit0 bit1 + not(bit0 +bit1))
#### Figure 2: Circuit
![IMG_0486](https://user-images.githubusercontent.com/105724334/203496207-490b52e0-03f3-41e9-8a15-f7f2c6c1649b.jpg)

