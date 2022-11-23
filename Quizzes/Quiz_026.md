## Quiz 26
#### Program code
Create a program that shows the graph of the data and create a linear (H_model = m*h + b) model for the data

```.py
import matplotlib.pyplot as plt
import numpy as np
h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0,
         51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
x = []
for i in range(len(h)):
    x.append(i)

plt.scatter(x, h, color="#FF00FF")
plt.ylabel("Relative Humidity %")
plt.xlabel("Samples")
plt.title ("Humidity on Campus (Nov. 15)")

m, b = np.polyfit(x, h, 1)
print(f"Linear Equation: y = {m:.2f}h + {b:.2f}")
h_model = []
y_model = []
for i in [1,32]:
    h_model.append(i)
    y_model.append(m*i+b)
plt.plot(h_model,y_model, color="#117A65")
plt.text(5, 55.5, f"y = {m:.2f}h + {b:.2f}")

plt.show()
```

#### Figure 1: Proof of code
<img width="618" alt="Screen Shot 2022-11-23 at 17 50 17" src="https://user-images.githubusercontent.com/105724334/203504802-60108c67-e50e-45a1-9b75-54c1005aaa02.png">

#### Convert color in hex to rgb
#e6e627
#### Figure 2: Color conversion 
![IMG_94208B74B04B-1](https://user-images.githubusercontent.com/105724334/203507029-b585c349-e459-45a9-a31f-482c98106a43.jpeg)

