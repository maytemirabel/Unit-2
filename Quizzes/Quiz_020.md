## Quiz 20 - 
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
