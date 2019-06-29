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

    var num = 1...150

    for i in num {
        print(i)
    }

***
## Question 2

Write code that prints all the numbers from 142 to 159, **exclusive.**

    var num = 142..<159
 
    for i in num {
        print(i)
        }
***
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**

    var num = 15...80

    for i in num where i % 2 == 0 {
    print(i)
    }

***
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**

    var num = 19...51

    for i in num where i % 2 == 1 {
    print(i)
    }

***
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**

    var num = 1..<100

    for i in num where i % 10 == 5 {
        print(i)
    }
***
## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**

    var num = 1...40

    for i in num where i % 10 == 7 {
        print(i)
    }

***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`

    var num = 20...150
    
    for i in num where  i % 3 == 0 {
    print(i)
    }


***
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`

    var num = 20...150

    for i in num where (i % 3 == 0) && (i % 2 == 0) {
        print(i)
    }

***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`

    var num = 20...150

    for i in num where i % 10 == 4 {
        print(i)
    }

***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`

    var num = 20...150

    for i in num {
        if i == 31 || i == 35  {
            print(i)
            continue
        }
        if (i >= 40 && i <= 60){
            print(i)
        }
    }



***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.

```swift
var i = 5

while (i > 3) {
    i += 1
}

// Your explanation here
```
The loop will run an infinite number of times. The while loops runs as long as the condition is true. Since i starts out being greater than 3 and it continues to increase by 1 the condition statement will always be true. 

***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5

while (i < 9) {
    i += 1
}
```

***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 5

while (i < 1,005) {
    i += 1
}
```

***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5

while (i < 1005) {
    if (i % 2 == 0){
        print(i)
    }
    i += 1
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
The first while loop evaluates the condition first and prints only if the condition is true. The second while loop (repeat-while loop) first prints the statement and then evaluates the condition. In this case the output will be the same because the condition starts out being true for both loops. 
## Question 16

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.


Continue lets you end that iteration of the loop but brings you to the next iteration of the loop. Break ends the loop entirely. 

    var range = 1...10

    for i in range {
        if i == 5 {
            continue
        }
        print(i)
    }
    
    var range2 = 1...10
    
    for i in range2 {
        if i == 5 {
            break
        }
        print(i)
    }



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

[x]1
[x]2
[x]3
[]4
[]5
[]6
[]7
[x]8
[x]9
[x]10



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

[x]1
[x]2
[x]3
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
This loop will print 1, 2 & 3 for X but it will only print 1 for Y.  The loop first starts with the 1 in X, then it sees there's a 1 for Y. Since the if condition is false, it will continue to the next line of code so it will print "x = 1, y =1". It will then continue with the 1 in the X loop and go to the next iteration in the Y loop which is 2. Since the if statement is now true it will run the block of code inside the if statement. The block of code says to continue to the outerloop so instead of printing Y or going to the next iteration of Y, it goes to the next iteration of the X loop which is 2. X=2, Y=1 will print and it will again go to the next interation for the X loop. 

This is what it will print: 
x = 1, y = 1
x = 2, y = 1
x = 3, y = 1

***
## Question 20

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.

    var xRange = 0...10
    var yRange = 0...10

    for x in xRange {
    for y in yRange{
    print("(\(x), \(y))")
    }

    }

***
## Question 21

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.

    var xRange = 0...10
    var yRange = 0...10

    for x in xRange {
        for y in yRange where abs(x - y) >= 5 {
            print("(\(x), \(y))")
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

var N = 5
var num = 1

while num <= N  {
    print(num * num)
    num += 1
}

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

var N = 2
var range1 = 1...N


    for _ in range1 {
        for _ in range1 {
            print("*",terminator: " ")
        }
    print("")
    }

```

Example 2:
Input: `var N = 3`

Output:
```swift
***
***
***

var N = 3
var range1 = 1...N

for _ in range1 {
    for _ in range1 {
        print("*",terminator: " ")
    }
    print("")
}

```

Hint 1
Try printing a single line of * first.

Hint 2
You can use print("") to print an empty line.

***
