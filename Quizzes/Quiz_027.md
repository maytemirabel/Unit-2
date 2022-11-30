## Quiz 27
#### Program code
Create a errorbar graph for the data below. You will need to calculate the mean and standard deviation first.

```.py
import matplotlib.pyplot as plt
import numpy as np
plt.style.use('ggplot')
sensorA = [16, 24, 24, 9, 23, 26, 26, 23, 25, 14]
sensorB = [2, 19, 25, 10, 11, 24, 17, 7, 24, 17]
sensorC = [15, 11, 24, 21, 6, 2, 18, 27, 1, 16]

samples = []
for i in range (len(sensorA)):
    samples.append(i)

fig = plt.figure(figsize=(8,4))
plt.subplot(1,2,1)

plt.plot(samples, sensorA, color = "#52796f")
plt.plot(samples, sensorB, color = "#9b2226")
plt.plot(samples, sensorC, color = "#073b4c")
plt.xlabel("Samples")
plt.ylabel("Values")
plt.title("Sensors (A, B, C)")

mean_list = []
standard_dev = []
high = []
low = []

for i in range (len(sensorA)):
    data = [sensorA[i], sensorB[i], sensorC[i]]
    mean_list.append(np.mean(data))
    standard_dev.append(np.std(data))
    high.append(np.max(data))
    low.append(np.min(data))

plt.subplot(1,2,2)
plt.plot(samples, mean_list, color = "#003049")
plt.fill_between(samples, high, low, alpha = 0.5, color = "#264653")
plt.errorbar(samples, mean_list, standard_dev, fmt = "o")

plt.show()

``` 

#### Figure 1: Proof of program
<img width="793" alt="Screen Shot 2022-11-25 at 11 03 40" src="https://user-images.githubusercontent.com/105724334/203885674-bea4867f-26c3-4f26-bbd5-1f3031e6e574.png">

#### Convert the following rgb color to hex color 
red=250, green=100, blue=10

#### Figure 2: Conversion 
![IMG_0508](https://user-images.githubusercontent.com/105724334/204752047-796de01e-3c08-4d95-b2c8-e4d1a1d324ed.jpg)
