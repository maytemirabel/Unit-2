## Quiz 18 - Lily
#### Program code
Create a function to help Lily

Program using an equation
```.py
def numberMatches(length:int, seconds:int)->int:
    return length * 100 / seconds / 5
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

#### Figure 1: Proof of program (equation program)


#### Figure 2: Proof of program (while loop)
<img width="410" alt="Screen Shot 2022-11-02 at 17 12 39" src="https://user-images.githubusercontent.com/105724334/199435392-7201ebeb-14cb-4429-87ba-a208d2b8d044.png">

#### Figure 3: Flowchart of program (while loop)
