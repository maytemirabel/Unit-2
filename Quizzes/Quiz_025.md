## Quiz 25
#### Program code
Code a program that shows the graoh of the function below for 100 values of x in the interval -10 < x < 10
```.py
from matplotlib import pyplot as plt
def absolute():
    x_out = []
    y_out = []
    st = -10
    for i in range(101):
        x_out.append(st)
        y = abs(st)
        y_out.append(y)
        st += 0.2

    return x_out, y_out

data_x, data_y = absolute()
plt.ylabel('$f(x) = |x|$')
plt.xlabel('x')
plt.plot(data_x, data_y)
plt.show()
``` 

#### Figure 1: Proof of program
<img width="627" alt="Screen Shot 2022-11-15 at 13 39 31" src="https://user-images.githubusercontent.com/105724334/201827778-65f38313-1f16-4b15-bcae-fc093c962b84.png">

#### Convert to decimal 
FFA5 
#### Figure 2: Hexadecimal to decimal conversion 
![IMG_0488](https://user-images.githubusercontent.com/105724334/203499038-296f03d1-7e17-4e88-98fc-5d64f0d97ba3.jpg)

