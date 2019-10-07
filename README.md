# Optionals lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

a. Given the variable `userNameOne` below, print *"The username is Test User"*.  Use *Optional Binding* (`if let`) to print the name.

```swift
var userNameOne: String? = "Test User"

//Answer:

if let user = userNameOne {
    print("The username is \(user)")
}
```

b. Given the variable `userNameTwo` below, print *"The username is undefined"*.  Use the *nil coalescing operator* (`??`).

```swift
var userNameTwo: String? = nil

//Answer:

print("The username is \(user2)")
```

## Question 2

a. Given the variables `rectOneWidth` and `rectOneHeight` below, print "The area of rectOne is 50".  Use *Optional Binding* (`if let`) to print the area.

```swift
var rectOneWidth: Double? = 5
var rectOneHeight: Double? = 10

//Answer:

if let width = rectOneWidth, let length = rectOneHeight {
    let area = length * width
    print("The area of rectOne is \(area)")
}
```

b. Given the variables `rectTwoWidth` and `rectTwoHeight` below, print "The area of rectTwo is not able to be calculated".  Use *Optional Binding* (`if let`) to print this message.

```swift
var rectTwoWidth: Double? = nil
var rectTwoHeight: Double? = nil

//Answer:

if let width = rectTwoWidth, let height = rectTwoHeight {
    let area = height * width
    print("rect two area: \(area)")
} else {
    print("The area of rectTwo is not able to be calculated")
}

```

## Question 3

a. Given the variables `userOneName`, `userOneAge`, and `userOneHeight` below, write code that prints "Hello Anne!  You are 15 years old and 5.8 feet tall" (1 foot = 12 inches).  Use optional binding.


```swift
var userOneName: String? = "Anne"
var userOneAge: Int? = 15
var userOneHeight: Double? = 70

//Answer:

if let name = userOneName, let age = userOneAge, let height = userOneHeight {
    print("Hello \(name)! You are \(age) years old and \(String(format: "%.1f", (height/12))) feet tall.")
}
```

b. Given the variables `userTwoName`, `userTwoAge` and `userTwoHeight` below, write code that prints "Hello user!  You are 15 years old and I don't know how tall you are".  Use optional binding

```swift
var userTwoName: String? = nil
var userTwoAge: Int? = 15
var userTwoHeight: Double? = nil

//Answer:

if let name = userTwoName, let age = userTwoAge, let height = userTwoHeight {
    print("Hello \(name)! You are \(age) years old and \(String(format: "%.1f", (height/12))) feet tall.")
} else {
    print("Hello user! You are 15 years old and I don't know how tall you are.")
}
```

## Question 4

Given the variable `favoriteNumber`, write code that either prints "Your favorite number is " followed by the number, or "I don't know what your favorite number is"

`favoriteNumber` is of type Int? and will either be `nil` or a random number between 0 and 10.  It will change each time you run your Playground.

```swift
var favoriteNumber = Bool.random() ? Int.random(in: 0...10) : nil

// Answer: 

if let yourNum = favoriteNumber {
    print("Your favorite number is \(yourNum)")
} else {
    print("I don't know what your favorite number is")
}
```

## Question 5

Given the variables `numOne`, `numTwo` and `numThree`, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numOne = Bool.random() ? Int.random(in: 0...10) : nil
var numTwo = Bool.random() ? Int.random(in: 0...10) : nil
var numThree = Bool.random() ? Int.random(in: 0...10) : nil

//Answer:
var numArray = [Int?]()
numArray.append(numOne)
numArray.append(numTwo)
numArray.append(numThree)

var sum = 0
for num in numArray {
    if let validNum = num{
        sum += validNum
    }
}
print("The sum is \(sum)")

```

## Question 6

a. Given the variable `numbers` below, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numbers = [Int?]()

for _ in 0..<10 {
    numbers.append(Bool.random() ? Int.random(in: 0...100) : nil)
}

//Answer:

var sum = 0
for num in numbers {
    if let validNum = num{
        sum += validNum
    }
}
print("The sum is \(sum)")

```

b. Using the same variable, find the average of all non-nil values.

```swift

var sum = 0
var countNonNils = 0
for num in numbers {
    if let validNum = num{
        sum += validNum
        countNonNils += 1
    }
}
let average = sum/countNonNils
print("The average is \(average)")

```
## Extra Questions

https://github.com/joinpursuit/Pursuit-Core-iOS-Extra-Optionals-Questions/blob/master/README.md
