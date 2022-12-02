## Quiz 31
#### Program code
Create a graph for the x, y data
```.py
import requests
from matplotlib import pyplot as plt
import numpy as np
plt.style.use("ggplot")

req = requests.get("http://192.168.6.142/readings")
data = req.json()
readings = data ["readings"][0]
print(readings)

temp = []
samples = []
for r in readings:
    if r["sensor_id"] ==1:
        temp.append(r["value"])

temp = temp[610:800]

for i in range(len(temp)):
    samples.append(i)

#linear model
m, b = np.polyfit(samples, temp, 1)
x_lineal = []
y_lineal = []
for i in [0,190]:
    x_lineal.append(i)
    y_lineal.append(m*i+b)

plt.scatter(samples, temp)
plt.plot(x_lineal, y_lineal)
plt.xlabel("Samples")
plt.ylabel("Temperature")
plt.show()
``` 

#### Figure 1: Proof of program
<img width="644" alt="Screen Shot 2022-12-02 at 15 31 50" src="https://user-images.githubusercontent.com/105724334/205230178-4b676066-50c6-4db2-8d22-a3c6dcb737f4.png">
