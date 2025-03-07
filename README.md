## Mid Unit-1 Review


## Strings

1. **Given a String, return a String with each letter uppercased**

Input: `Hello, there`

Output: `HELLO, THERE`
```
My Answer !! 
var string = "Hello, there"
print(string.uppercased())
```

2. **Given a String, return a String alternating between uppercase and lowercase letters**


Input: `Hello, there`

Output: `HeLlO, tHeRe`
```
My Answer:
var output = ""
func alternatedUpperandLowerCase(for words: String) -> String {
    for (num,letter) in words.enumerated() {
    if num % 2 == 1
    output.append(letter.lowercase())
    
    } else if num % 2 == 0 {
    output.append(letter.uppercase)
}
    return String()
    }
```

3. **Given a String, return a String with all occurrences of a given letter removed**

Input: `Hello, there`

Output: `Hllo, thr`
```
My Answer :
var input = "Hello There"
var output = ""
var letter = "e"
for char in input where String(char) != letter {
    output.append(char)
        
    }

```
## Arrays


1. **Given an array of type [Int], return the largest element**

Input: `[1,5,2,4,1,4]`

Output: `5`
```
My Answer: 
var largestArray = [1,5,2,4,1,4]

var maxRan = largestArray.max() ?? 0
print(maxRan)
```

2. **Given an array of type [Int], return the smallest element**

Input: `[1,5,2,4,1,4]`

Output: `1`

```
My Answer:

var smallestArray = [1,5,2,4,1,4]

var minRan = smallestArray.min() ?? 0
print(minRan)
```

3. **Given an array of type [Int], return its sum**

Input: `[1,5,2,4,1,4]`

Output: `17`

```
My Answer
var totalSum = [1,5,2,4,1,4]
print(totalSum.reduce(0,+))

```

4. **Given an array of type [Double], return its average**

Input: `[3,4.5,7.5,2,1]`

Output: `3.6`
```
My Answer:
var averageArray = [3,4.5,7.5,2,1]
let firstNum = averageArray.reduce(0,+) // this addes all the numbers together
let secNum = Double(averageArray.count) // this counts the numbers in the array
let avgAns = firstNum / secNum
print(avgAns)
```

5. **Given an array of type [Double] and a Double, return the sum of all numbers in the array greater than a given number**

Input: `[3,4.5,7.5,2,1], 3`

Output: `12`

```
My answer:
var sumofDoubles = 0.0
let arrayofDoubles = [3,4.5,7.5,2,1]
for num in arrayofDoubles{
    if num > 3{
    sumofDoubles += num
    }
}
print(sumofDoubles)
```


6. **Given an array of type [Double], return the product of all the elements**

Input: `[3,4.5,7.5,2,1]`

Output: `202.5`

```
My Answer:
var multiple = 1.0
let array = [3,4.5,7.5,2,1]
for num in array{
    multiple *= num
    }
print(multiple)
```

7. **Given an array of type [Int], return the second smallest value in the array**

Input: `[3,6,1,9,4,8]`

Output: `3`

My answer:

```
let array = [3,6,1,9,4,8].sorted()
print(array[1])
```

## Optionals

1. **Given an array of type [String?] return an array of [String] removing all nil values**
// may or may not contain value 
// return = function 
Input: `[nil, "We", "come", nil, "in", "peace"]`

Output: `["We", "come", "in", "peace"]`

```
My answer:
var array = [nil, "We", "come", nil, "in", "peace"]
var newArray = [String]()
for str in array {
    if let unwrapStr = str {
        newArray.append(unwrapStr)
    } else {
        print("not valid value, \(String(describing: str))")
    }
}
print(newArray)



notes:

// optional binding 
func returnNonNil(arrayOfInput:[string?]) -> [String]{
for word in arrayOfInput{
if let unwrappedWord = word {
output.append(unwrappedWord)
}
}
return output
}

// neo co
var output = [String]()
var input = [nil, "We", "Come", nil, "in","Peace"]
func returnNonNilValue(arr: [String?]) -> [String]{
    for word in arr {
        output.append(word ?? " ")
    }
    return output
}
//Bang dont use it unless 
//var output = [String]()
//var input = [nil, "We", "Come", nil, "in","Peace"]
//func returnNonNilValue(arr: [String?]) -> [String]{
//    for word in arr {
//        output.append(word!)
//    }
//    return output
//}
```


2. **Given an array of type [String?]? return an array of [String] removing all nil values**

Input: `nil`

Output: `[]`

My Answer:
```
let removingnil = [String?]()
let nonNillArray = array.filter({$0 != nil})
print(nonNillArray)
```
3. **Given an array of type [Int?] return the sum of all non-nil values.  Use guard statements in your solution.**

Input: `[4, nil, 9, 5, nil]`

Output: `18`

My Answer:

```
var inputWithNil = [4, nil, 9, 5, nil]
var nonNil = 0

for num in inputWithNil {
   if num != nil {
        nonNil += num!
    }
}
print(nonNil)
```

4. **Given an array of type [Int?]? return the sum of all non-nil values.  Use guard statements in your solution.**

Input: `nil`

Output: `0`

5. **Given an array of type [Int?] and an optional Int, return the sum of all values not equal to the given number.  If the given number is nil, return the sum of all non-nil values.**

Input: `[1, 1, nil, 3, 5, nil, 1, nil, 3, 5, nil, 5, nil, 3], 1`

Output: `24`


## Dictionaries

1. **Given an array of type [String], return a copy of the array with all duplicate values removed**

Input: `["apple", "apple", "banana", "banana", "banana", "cake", "cake"]`

Output: `["apple", "banana", "cake"]`

My Answer:

```

var words = ["apple", "apple", "banana", "banana", "banana", "cake", "cake"]

words = Array(Set(words))

print(words.sorted())

```

2. **Given a String, find the most frequently occurring letter**

Input: `Never trust a computer you can't throw out a window ~ Steve Wozniak`

Output: `t`

3. **Given an array of type [Int], return a copy of the array that contains only elements that appear at least twice**

Input: `[1,1,2,3,3,3,4,5,6,6,7]`

Output: `[1,3,6]`

4. **Given a String, find the second most frequently occurring letter in a string**

Input: `Never trust a computer you can't throw out a window ~ Steve Wozniak`

Output `o`


## Closures

1. **Given an array of type [String], return an array that contains the Strings sorted alphabetically with capital letters first (Swift will do that part automatically)**

Input: `["Never", "trust", "a", "computer", "you", "can't", "throw", "out", "a", "window"]`

Output: `["Never", "a", "a", "can\'t", "computer", "out", "throw", "trust", "window", "you"]`

2. **Given an array of type [String], return an array that contains the Strings sorted by length**

Input: `["Never", "trust", "a", "computer", "you", "can't", "throw", "out", "a", "window"]`

Output: `["a", "a", "you", "out", "Never", "trust", "can\'t", "throw", "window", "computer"]`

3. **Given an array of type [String], return an array containing all Strings at least 4 characters long**

Input: `["Never", "trust", "a", "computer", "you", "can't", "throw", "out", "a", "window"]`

Output: `["Never", "trust", "computer", "can\'t", "throw", "window"]`

4. **Given an array of type [String], return a String containing all of the Strings from the array combined and separated by spaces.  Do this first without using the `joined(separator:) method`**

Input: `["Never", "trust", "a", "computer", "you", "can't", "throw", "out", "a", "window"]`

Output: `Never trust a computer you can't throw out a window`


## Enums


1. **Given an array of type [Int] and an instance of NumberType (defined below), return an array containing only all the even or odd numbers.**

```swift
enum NumberType {
    case even
    case odd
}
```

Input: `[1,2,3,4,5,6], NumberType.odd`

Output: `[1,3,5]`

2. **Given a String and an instance of StringType (defined below), return the String either lowercased or uppercased**

```swift
enum StringType {
    case lowercase
    case uppercase
}
```

Input: `"Design is not just what it looks like and feels like. Design is how it works", .uppercase`

Output: ``"DESIGN IS NOT JUST WHAT IT LOOKS LIKE AND FEELS LIKE. DESIGN IS HOW IT WORKS"``

3. **Given an array of type [FileStatus] (defined below) and an Int, return an array containing only files that were saved more than that many times**

```swift
enum FileStatus: CustomStringConvertible {
    case unsaved
    case saved(numberOfVersions: Int)
    var description: String {
        switch self {
        case .unsaved: return "Unsaved File"
        case let .saved(numberOfVersions): return "File that has been saved \(numberOfVersions) times"
        }
    }
}
```

Input: `[FileStatus.saved(numberOfVersions: 5), FileStatus.saved(numberOfVersions: 3), FileStatus.saved(numberOfVersions: 8)], 4`

Output: `[File that has been saved 5 times, File that has been saved 8 times]`
