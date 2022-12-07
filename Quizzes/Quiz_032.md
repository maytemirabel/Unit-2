## Quiz 32
#### Program code
```.py
import requests
import matplotlib.pyplot as plt
req=requests.get('http://192.168.6.142/readings')
readings = req.json()['readings']
readings = readings[0]

temp9 = []
temp10 = []

for i in readings:
    if i['sensor_id'] == 9:
        temp9.append(i['value'])

for i in readings:
    if i['sensor_id'] == 10:
        temp10.append(i['value'])

smooth9 = []
smooth10 = []
number_samples_per_hour = 12

for i in range(0,len(temp9), number_samples_per_hour):
    data_in_window = temp9[i : i + number_samples_per_hour]
    average9 = sum(data_in_window) / number_samples_per_hour
    smooth9.append(average9)

for i in range(0, len(temp10), number_samples_per_hour):
    data_in_window = temp10 [i : i + number_samples_per_hour]
    average10 = sum(data_in_window) / number_samples_per_hour
    smooth10.append(average10)

x = []
for i in range(45):
    x.append(i+1)

difference = []

for i in range (len(smooth9)):
    d = smooth9[i]-smooth10[i]
    difference.append(d)

fig = plt.figure(figsize=(8, 5))
plt.subplot(3,1,1)
plt.plot(x, smooth9[0:45])
plt.title("Sensor 9")

plt.subplot(3,1,2)
plt.plot(x, smooth10[0:45])
plt.title("Sensor 10")

plt.subplot(3,1,3)
plt.plot(difference[0:45])
plt.title("Difference")
plt.tight_layout()
plt.show()

```

#### Figure 1: Proof of program
<img width="796" alt="Screen Shot 2022-12-08 at 0 26 35" src="https://user-images.githubusercontent.com/105724334/206220159-7ff3272f-a506-44ef-878c-e468be7b8551.png">

#### What are the three main operators used in boolean logic?
The three main operators are AND, OR, and NOT
