## Quiz 17 - Word Length
#### Program code
Code a function that produces the average word length of the input list
```.py
def averageLength (words:list) -> float:
    count = 0
    total = 0
    for x in words:
        total += len(x)
        count +=1
    return total / count
``` 

#### Figure 1: Proof of program
<img width="409" alt="Screen Shot 2022-10-25 at 14 11 44" src="https://user-images.githubusercontent.com/105724334/197699468-5f7148e1-58bd-4ec0-b5e1-7c3dcc40323e.png">

