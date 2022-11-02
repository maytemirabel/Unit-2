## Quiz 18 - Lily
#### Program code
Create a function to help Lily
```.py
def numberMatches(length :int, seconds :int):
    length = length * 100
    if ((length / seconds) % 5) == 0:
        out = ((length / seconds) / 5)
    else:
        out = (((length / seconds) // 5) + 1)
    return out
```

Program using a while loop 
```.py
def numberMatches (length:int, seconds:int) -> int:
    lily_position = 0
    speed_m_per_s = seconds/100
    seconds_passed = 0
    matches = 0
    while lily_position < length:
        seconds_passed += 1
        #move lily
        lily_position += speed_m_per_s
        if seconds_passed == 5:
            matches += 1
            seconds_passed = 0
    return matches

test1 = numberMatches(100,100)
print (test1)
```

#### Figure 1: Proof of program 
<img width="384" alt="Screen Shot 2022-11-02 at 19 44 16" src="https://user-images.githubusercontent.com/105724334/199470121-9bead51d-a65f-49b9-8a7e-a3fdab5de600.png">


#### Figure 2: Proof of program (while loop)
<img width="410" alt="Screen Shot 2022-11-02 at 17 12 39" src="https://user-images.githubusercontent.com/105724334/199435392-7201ebeb-14cb-4429-87ba-a208d2b8d044.png">

#### Figure 3: Flowchart of program (while loop)
<img width="341" alt="Screen Shot 2022-11-02 at 19 46 31" src="https://user-images.githubusercontent.com/105724334/199470568-fc2f3499-5983-446e-86f1-25ac786f84db.png">

