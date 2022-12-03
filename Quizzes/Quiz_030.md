## Quiz 30
#### Program code
```.py
from matplotlib import pyplot as plt
h = [54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
plt.style.use("dark_background")

x = []
y = []
samples_per_window = 4

for i in range (0, len(h), samples_per_window):
    data_in_window = h[i : i + samples_per_window]
    y.append(sum(data_in_window)/samples_per_window)
    x.append(i)

    y_overlap_50 = []
    x_overlap_50 = []
    for i in range (0, len(h), int(samples_per_window * 0.5)):
        data_in_window = h[i : i + samples_per_window]
        y_overlap_50.append(sum(data_in_window)/samples_per_window)
        x_overlap_50.append(i)

    plt.plot(x_overlap_50, y_overlap_50, "o-", color = "#a8dadc")
    plt.ylabel("Relative Humidity")
    plt.xlabel("Samples")
    plt.show()
```

#### Figure 1: Proof of program
<img width="627" alt="Screen Shot 2022-12-03 at 16 24 06" src="https://user-images.githubusercontent.com/105724334/205430006-d414b2f4-2223-4b3e-8534-e5aee42988ea.png">

#### When was the internet first created?
According to the University System of Georgia, the official birthday of the Internet is January 1st, 1983. Before this data, computer networks were not able to communicate with each other. 
(University System of Georgia, n.d.)
