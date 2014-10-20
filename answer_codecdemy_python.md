### answer of codecademy python

---
# Practice Makes Perfect


## is_even 
```python
def is_even(x):
    if x % 2 == 0:
        return True
    else:
        return False
```

## is_int
```python
mport types

def is_int(x):
    if x - round(x) == 0:
        return True
    else:
        return False
```

## digit_sum
```python
def digit_sum(n):
    x = 0
    while n  != 0:
       
        x += n % 10
        n = n / 10
    return x
```

## factorial
```python
def factorial(x):
    result = 1
    while x != 0:
        result *= x
        x = x-1
    return result
```

## is_prime
```python
def is_prime(x):
    count = 0
    x= int(x)
    if x <2:
        return False
    elif x==2:
        return True
    else :
        for i in range(2,x):
            if x % i == 0 :
                count += 1
        if count >= 1:
            return False
        else:
            return True
```

## reverse
```python
def reverse(text):
    strs=''
    lenth = len(text)
    while lenth > 0:
        strs+=text[lenth-1]
        lenth -= 1
    return strs
```

## anti_vowel
```python
def anti_vowel(text):
    strs=''
    for i in text:
        if i in 'aeiouAEIOU':
            continue
        else:
            strs += i
    return strs
```
## scrabble_score
```python
def scrabble_score(word):
    word = word + ""
    word = word.lower()
    
    score = {"a": 1, "c": 3, "b": 3, "e": 1, "d": 2, "g": 2, "f": 4, "i": 1, "h": 4, "k": 5, "j": 8, "m": 3, "l": 1, "o": 1, "n": 1, "q": 10, "p": 3, "s": 1,"r": 1, "u": 1, "t": 1, "w": 4, "v": 4, "y": 4, "x": 8, "z": 10}
    total=0
    for c in word:
        total += score.get(c)
    return total
```

## censor
```python
def censor(text,word):
    words=text.split()
    for i in range(len(words)):
        if words[i]==word:
            words[i]="*" * len(words[i])
    return " ".join(words)
```

## count
```python
def count(sequence,item):
    found = 0
    for i in range(len(sequence)):
        if sequence[i] == item:
            found += 1
    return found
```

## purify
```python
def purify(numbers):
    result = [ ]
    for i in range(len(numbers)):
        if numbers[i] % 2 == 0:
            result.append(numbers[i])
    return result
```

## product
```python
def product(integers):
    result = 1
    for i in range(len(integers)):
        result  *= integers[i]
    return result
```

## remove_duplicates
```python
def remove_duplicates(lists):
    result = [ ]
    for i in range(len(lists)):
        if i == 0:
            result.append(lists[i])
        else:
            if lists[i] not in result:
                result.append(lists[i])
    return result
```

## median
```python
def median(numbers):
    v=sorted(numbers)
    lenth = len(v)
    if lenth == 1:
        return v[0]
    elif lenth % 2 == 0:
        return (v[lenth / 2] + v[(lenth / 2) -1]) / (2.0)
        
    else:
        return v[lenth / 2]
```


---
# EXAM STATISTICS

## Print those grades
```python
grades = [100, 100, 90, 40, 80, 100, 85, 70, 90, 65, 90, 85, 50.5]

def print_grades(grades):
    for i in grades:
        print i

print_grades(grades)
```

## The sum of scores
```python 
grades = [100, 100, 90, 40, 80, 100, 85, 70, 90, 65, 90, 85, 50.5]

def grades_sum(scores):
    total = 0
    for i in scores:
        total += i
    return total
print grades_sum(grades)
```

## Computing the Average
```python
grades = [100, 100, 90, 40, 80, 100, 85, 70, 90, 65, 90, 85, 50.5]

def grades_sum(scores):
    total = 0
    for i in scores:
        total += i
    return total
print grades_sum(grades)

def grades_average(grades):
    total = grades_sum(grades)
    average =  total / float(len(grades))
    return average
print grades_average(grades)
```

## The Variance
```python
grades = [100, 100, 90, 40, 80, 100, 85, 70, 90, 65, 90, 85, 50.5]

def print_grades(grades):
    for grade in grades:
        print grade

def grades_sum(grades):
    total = 0
    for grade in grades: 
        total += grade
    return total
    
def grades_average(grades):
    sum_of_grades = grades_sum(grades)
    average = sum_of_grades / float(len(grades))
    return average

def grades_variance(scores):
    average = grades_average(scores)
    variance = 0
    for score in scores:
        variance += ((average - score)**2)
    variance = variance / float( len(scores))
    return variance
print grades_variance(grades)
```

## Standard Deviation
```python 
grades = [100, 100, 90, 40, 80, 100, 85, 70, 90, 65, 90, 85, 50.5]

def print_grades(grades):
    for grade in grades:
        print grade

def grades_sum(grades):
    total = 0
    for grade in grades: 
        total += grade
    return total
    
def grades_average(grades):
    sum_of_grades = grades_sum(grades)
    average = sum_of_grades / float(len(grades))
    return average

def grades_variance(scores):
    average = grades_average(scores)
    variance = 0
    for score in scores:
        variance += ((average - score)**2)
    variance = variance / float( len(scores))
    return variance
print grades_variance(grades)

def grades_std_deviation(variance):
    return variance ** 0.5

variance = grades_variance(grades)
print grades_std_deviation(variance)
```

## Review
```python
grades = [100, 100, 90, 40, 80, 100, 85, 70, 90, 65, 90, 85, 50.5]

def print_grades(grades):
    for grade in grades:
        print grade
print_grades(grades)
def grades_sum(grades):
    total = 0
    for grade in grades: 
        total += grade
    return total
print grades_sum(grades)    
def grades_average(grades):
    sum_of_grades = grades_sum(grades)
    average = sum_of_grades / float(len(grades))
    return average
print grades_average(grades)
def grades_variance(scores):
    average = grades_average(scores)
    variance = 0
    for score in scores:
        variance += ((average - score)**2)
    variance = variance / float( len(scores))
    return variance
print grades_variance(grades)

def grades_std_deviation(variance):
    return variance ** 0.5

variance = grades_variance(grades)
print grades_std_deviation(variance)
```

---
