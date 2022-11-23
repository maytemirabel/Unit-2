## Quiz 29
#### Program code

```.py
def count_letters(lexicon, msg):
    for letter in (msg):
        if letter in lexicon.keys():
            lexicon[letter]+=1
    return lexicon

consonants = {"w": 0, "c": 0, "l":0}
case1 = count_letters(consonants, "hello world")
print (case1)

vowels = {"a": 0, "e": 0, "i":0, "o": 0, "u":0}
case2 = count_letters(vowels, "Why did I choose CS?")
print (case2)
``` 

#### Figure 1: Proof of program
<img width="427" alt="Screen Shot 2022-11-24 at 8 23 10" src="https://user-images.githubusercontent.com/105724334/203662672-7017178f-b032-4ec4-8146-675ecd096089.png">


#### How many different colors could be presented in a 6 bit computer?
