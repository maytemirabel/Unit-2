## Quiz 21 - 
#### Program code
Using the function that produces the table of Truth for 3 inpuuts, add a column for the boolean equation.

```.py
def get_truth ():
    print ("| C | B | A | AB + not B + not CB |")
    print ("- " * 18)

    for x in range (8):
        a = x // 4
        b = (x % 4) // 2
        c = x % 2
        d = int(a and b) or int(not b) or int(not b and c)
        print (f"| {a} | {b} | {c} |          {d}          |")

table = get_truth()
print (table)
```

#### Figure 1: Proof of program
<img width="507" alt="Screen Shot 2022-11-07 at 13 33 15" src="https://user-images.githubusercontent.com/105724334/200227216-95d162d0-3686-4f1b-8608-b2610b970cf8.png">
