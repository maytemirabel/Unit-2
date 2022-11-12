## Quiz 20 - Get Truth
#### Program code
Create a function that produces the table of truth for 3 inputs

```.py
def get_truth ():
    print ("| A | B | C |")
    print (" - " * 4)
    for x in range (8):
        a = x // 4
        b = (x % 4) // 2
        c = x % 2
        print (f"| {a} | {b} | {c} |")
table = get_truth()
print (table)
```

#### Figure 1: Proof of program
<img width="316" alt="Screen Shot 2022-11-02 at 17 40 22" src="https://user-images.githubusercontent.com/105724334/199440882-657662e4-dfa1-472a-9014-737d5b7117fc.png">

#### Truth Table & Boolean Circuit
Equation: Light = S1S2+(S2+S3(notS1))S1 

#### Figure 2: Truth Table
![IMG_0460](https://user-images.githubusercontent.com/105724334/201461260-ab8f2aa0-6a1b-4543-992b-b6cc16d09d54.jpg)

#### Figure 3: Circuit 
![IMG_0461](https://user-images.githubusercontent.com/105724334/201461261-251e76da-71f6-4c53-9260-732687929c0d.jpg)
