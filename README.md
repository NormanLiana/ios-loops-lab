# Loops Lab

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit


## Question 1

Write code that prints all the numbers from 1 to 150, **inclusive.**

```swift
let numbers = 1...150

for number in numbers {
print(number)
}
```


***
## Question 2

Write code that prints all the numbers from 142 to 159, **exclusive.**

```swift
let numbers = 142..<159

for number in numbers {
print(number)
}
```

***
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**

```swift
let numbers = 15...80

for number in numbers where number % 2 == 0 {
print(number)
}
```

***
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**

```swift
let numbers = 19...51

for number in numbers where number % 2 != 0 {
print(number)
}
```

***
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**

```swift
let numbers = 1..<100

for number in numbers {
if number % 2 != 0 && number % 5 == 0 {
print(number)
}
}
```

***
## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**

```swift
let numbers = 1...40
var checker = 7

for _ in numbers {
    if checker <= 40 {
        print(checker)
        checker += 10
    }
}
```

***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`

```swift
let numbers = 20...150

for number in numbers where number % 3 == 0 {
print(number)    
}
```

***
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`

```swift
let numbers = 20...150

for number in numbers where number % 2 == 0 && number % 3 == 0 {
print(number)
}
```

***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`

```swift
let numbers = 20...150
var checker = 24

for _ in numbers {
if checker <= 150 {
print(checker)
checker += 10
}
}
```
***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`

```swift
var numbers = 20...150

for number in numbers {
if number == 31 || number == 35 || number == 40 || number == 60 {
print(number)
}

}
```

***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.

```swift
var i = 5

while (i > 3) {
    i += 1
}
```
// This will be an infinite loop. The loop says that while "i" (which is a variable and its value is 5) is greater than 3 run this code in the loop--> i = i + 1 which in the first loop would return a number of 6 to update "i" to 6. The loop would then run again because 6 is greater than 3 and this will continue on because in the statement of the loop we are always adding 1 to "i" so it will always be more than 3 in the condition meaning the loop will run over and over and will not stop.

***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5

while (i > 3) {
i += 1
if i == 9 {
break
}
}
```

***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 5

while (i > 3) {
i += 1
if i == 1005 {
break
}
}
```

***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5

while (i > 3) {
i += 1
if i % 2 == 0 {
print(i)
}
else if i == 1005 {
break
}
}
```

***
## Question 15

What's the difference in syntax between the following two while loops?  Will their outputs be different?  Explain why or why not.

```swift
var i = 1
//loop one
while i <= 10 {
    print("i = \(i)")
    i += 1
}

//loop two
var i = 1

repeat {
    print("i = \(i)")
    i += 1
} while i <= 10
```

//The syntax for loop one will check if the condition of the loop is true prior to running the loop whereas loop two repeats the loop prior to checking if the condition is true. Both loops have the same output because they both have the same statement for the loop as well as the same condition to check against its truth. They just check the condition and repeat the loop in a different order.


***
## Question 16

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.

"Break" tells you to completely stop the execution of a loop/if/switch. Whereas "continue" tells you to not execute that iteration of the loop and to go back to the beginning of the loop to perform the loop again.

```swift
// Continue example

var example = 2

while example < 7 {
example += 1
if example == 6 {
continue
}
print("\(example)")
}


// Break example

var example = 2

while example < 7 {
example += 1
if example == 6 {
break
}
print("\(example)")
}
```
***
## Question 17

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        continue
    }
    print(i)
}
```

[]1-This will print
[]2-This will print
[]3-This will print
[]4
[]5
[]6
[]7
[]8-This will print
[]9-This will print
[]10-This will print

***
## Question 18

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        break
    }
    print(i)
}
```

[]1-This will print
[]2-This will print
[]3-This will print
[]4
[]5
[]6
[]7
[]8
[]9
[]10

***
## Question 19

Without using Xcode, what will the loop below print?  Explain below.

```swift
outerloop: for x in 1...3 {
    innerloop: for y in 1...3 {
        if y == 2{
            continue outerloop
        }
        print("x = \(x), y = \(y)")
    }
}

//Answer below

x = 1, y = 1
x = 2, y = 1
x = 3, y = 1

//The outerloop assigns "x" to each number in the range of 1 through 3 (1, 2, 3). It starts at 1 for the outerloop and goes down to the innerloop where the same applies however "y" is assigned to the range of numbers (1, 2, 3) in the innerloop. The innerloop also starts at 1. It then takes the value of "y" (being 1 for this pass) and checks it in the condition in the line below. Is "y" (1) equal to 2? No it is not, making it false. Thus not executing the statement in the line below for that condition. It moves down to print, which will print out "x = 1, y = 1". It then moves to the innerloop to complete the next two passes of the innerloop. The next number for the innerloop is 2. It checks the condition in the line below and sees that y is equal to 2 (meaning it is true) so it performs the "continue outerloop" statement bringing it back to the outerloop where it then makes x equal to the next number in the range (2). The innerloop must now start from the first number in its range since the loop had been stopped and redirected to the outerloop. It will then print "x = 2, y = 1" since y is not equal to 2 in this pass. It will then go back to the innerloop with x equal to 2 and y equal to 2 but it will redirect back to the outerloop because y is equal to 2. The same will apply for the last pass of the outerloop. Where x is equal to 3. Thus printing out only "x = 3, y = 1". 
```

***
## Question 20

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.

***
## Question 21

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.

***
## Question 22

Print the first `N` square numbers. A **square number**, also called perfect square, is an integer that is obtained by squaring some other integer; in other words, it is the product of some integer with itself (ex. 1 = 1*1, 4 = 2 * 2, 9 = 3* 3 …).

Example:
Input: `var N = 5`

Output:
```swift
1
4
9
16
25
```

***
## Question 23

Given an integer N draw a square of N x N asterisks. Look at the examples.

Example 1:
Input: `var N = 2`

Output:
```swift
**
**
```

Example 2:
Input: `var N = 3`

Output:
```swift
***
***
***
```

Hint 1
Try printing a single line of * first.

Hint 2
You can use print("") to print an empty line.

***
