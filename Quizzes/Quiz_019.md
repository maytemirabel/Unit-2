## Quiz 19
#### Program code
Create a function that changes the vowels in a string to numbers such as a = 4, e = 3, i = 1, o = 0 and space by _

```.py
def get_l3tt3r(msg:str)-> str:
    new_msg = " "
    vowels = {"a": "4", "e" : "3", "i" : "1", "o" : "0", " " : "_"}
    for i in msg:
        if i in vowels.keys():
            i = vowels.get(i)
        new_msg+=i
    return ''.join(new_msg)
```

#### Figure 1: Proof of program
<img width="539" alt="Screen Shot 2022-11-02 at 17 20 03" src="https://user-images.githubusercontent.com/105724334/199436596-2fb58998-fd20-491b-b39f-eaec621f48fb.png">

#### Boolean Circuit 
Equation: AB + not(B+C) + B(notC notA)
#### Figure 2: Circuit 
![IMG_0456](https://user-images.githubusercontent.com/105724334/201458713-60a56cc8-5e4e-42c7-823b-0257f5c18c3d.jpg)
