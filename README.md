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

let numberLoop = 1...150
for Loop in numberLoop {
print(Loop)
}

***
## Question 2

Write code that prints all the numbers from 142 to 159, **exclusive.**

let numberLoop = 1..<159
for Loop in numberLoop {
if Loop <= 141 {
continue
}
print(Loop)

}
***
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**

let Loop = 15...80

for numbers in Loop where numbers % 2  == 0 {
print(numbers)
}

***
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**

let Loop = 15...51
for numbers in Loop where numbers % 2 != 0 {
print(numbers)
}

***
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**

let numberLoop = 1..<100
for numbers in numberLoop where numbers % 5 == 0 && numbers % 2 != 0  {
print(numbers)
}

***
## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**

let range = 1...40
var initialNum = 7
let maxNum = 40
for _ in range {
if initialNum < maxNum {
initialNum += 10
print(initialNum)
}

***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`

let numLoop = 20...150
for Loop in numLoop where Loop % 3 == 0 {
print(Loop)
}

***
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`

Numbers that are divisible by 2 and 3

let numLoop = 20...150
for Loop in numLoop where Loop % 2 == 0 && Loop % 3 == 0 {
print(Loop)
}


***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`

let range = 20...150
let maxNumber = 140
var initialNumber = 24
for _ in range where initialNumber < maxNumber {
initialNumber += 10
print(initialNumber)
}

***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`

let range = 20...150
var intiialNum = 40
let maxNum = 60

for num in range where num == 31 {
print(num)
}
for num in range where num == 35 {
print(num)
}
print(intiialNum)
for _ in range where intiialNum < maxNum {
intiialNum += 1
print(intiialNum)
}

***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.

infinitely, there's nothing to indicate an end to the loop.

```swift
var i = 5

while (i > 3) {
    i += 1
}




```
infinitely, there's nothing to indicate an end to the loop.

***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5

while (i > 3) {
    i += 1
}
```
var i = 5

while (i < 9) {
i += 1
print(i)
}
***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 5

while (i > 3) {
    i += 1
}
```
var i = 5

while (i < 1005) {
i += 1
print(i)
}
***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5

while (i > 3) {
    i += 1
}
```
while (i < 1005) {
i += 1
if i <= 1003 {
print(i)

} else if i >= 1003 && i % 2 == 0 {
print(i)
} else {
print("")
}
}



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
the result will be the same because 'while' and 'repeat' both loop.
while evaluates the condition of the loop at the start of each pass through but repeat-while evaluates its condition at the end of each pass through the loop.
***
## Question 16

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.

CONTINUE EXAMPLE

let loopExample = 1...10
for n in loopExample {
if n <= 6 && n <= 7 {
continue
}
print(n)
}


[continue] ends the current iteration of the loop but doesn't end the execution of the loop. This will print 7, 8 , 9 and 10 because [continue] only applies to n when it is <= 6 and <= 7. 

BREAK EXAMPLE

let loopExample = 1...10
for n in loopExample {
if n >= 5 {
break
}
print(n)
}

[break] ends the execution of the loop. This will print 1,2,3,4 because once n is >= 5 the loop will break.
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

[√]1
[√]2
[√]3
[]4
[]5
[]6
[]7
[√]8
[√]9
[√]10

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

[√]1
[√]2
[√]3
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
```
x = 1 y = 1
x = 2 y = 1
x = 3 y = 1

y == 2 will make the y value stay at y = 1 while the x value increase by 1 every loop. 
***
## Question 20

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.

for x in 0...10 {
for y in 0...10 {


print("x is \(x) , y is \(y)")
}
}
***
## Question 21

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.

for x in 0...10 {

for y in 0...10 {
if x - y >= 5 || y - x >= 5 {
print("x = \(x) , y = \(y)")
}
}
}
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
var n = 5
let loop = 1...n
for num in loop {

print(num * num)

}
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
