# Tool Learning Log

## Tool: **Swift**

## Project: **Brain Stimulating IOS App**

---

### 9/30/25:
* I looked over the [Swift documentation](https://www.swift.org/documentation/) for 15 minutes to try and get a gist of the tool

* I downloaded VS Code and installed a Swift extension to import all of its features.
    * I also watched this [tutorial](https://www.youtube.com/watch?v=J239BhLvOCA) to serve as a reference point during the installation process.
    * I created a new folder in File Explorer called SwiftProjects and imported it into VS Code.
* I created my first text using the `print` statement:

    ``` Swift
    print("Hi, my name is Joe")
    ```
* I also declared a variable, name, using `var` and assigned it a value of "Joe". Afterward, I created a `print` statement:

    ``` Swift
    var name = "Joe"
    print(name)
    ```
Note: Semicolons are optional in Swift. However, it drastically improves readability, which is beneficial when you have to debug your code. Some concepts in Swift are very similar to JavaScript.

* At last, I changed the value of my original variable by using the `=` constructor to reassign its value:

    ``` Swift
    var name = "Joe"
    print(name)
    name = "Hi World"
    ```

For next week: Explore more syntax and watch more tutorials on Youtube regarding Swift basics

### 10/27/25
* I watched the basics #2 video from a [Swift Youtube playlist](https://www.youtube.com/playlist?list=PLwvDm4VfkdpiLvzZFJI6rVIBtdolrJBVB) that went over the beginners level of coding
* I focused on the concept of Types. I started off with the `String` type where I created variables and set it to a value of the appropriate data type.
    * ``` Swift
        let helloWorld = "Hello World"

        let helloWorldOne = Hello World
      ```
NOTE: Like Java, Swift compiles code in order to run it. The second variable does not compile since the computer doesn't know exactly what the value is.

* I created my first set of boolean variables by declaring two variables. One that was directly set to a boolean value. The second one being declared with `:Bool` and then being set to a boolean value.
    *  ``` Swift
        let firstItem = true

        let firstItemOne: Bool = true
       ```
NOTE: In both cases, the variables are set to the value true. `:Bool` only declares the variable as a boolean type. The same can be applied to other types like strings.

* I tested out a new concept: `Date` type. I created a variable and set it equal to `:Date` type and `Date()`.
    * ``` Swift
        let myDate: Date = Date()
      ```

NOTE: The value of `Date()` is the current day, month, year, and time. It is considered **right now**.


* Afterwards, I tested out the `Number` data type. A Number could be represented as an `Int`, `Double`, `CGFloat`, and more.
    * ``` Swift
        let one = 1
        let two = 1.0
        let three = 1.0
      ```

NOTE: A `Float` is a number that can represent decimals. It is similar to a `Double`, but it is more limited to the amount of digits it can precise out.

* I also watched the Basics #3 video and created my first conditional in Swift:

``` Swift
let num: Bool = true
if num == true {
    print("num is true!")
}
```

NOTE: In Swift, conditionals do not use parenthesis to compare the conditions. It only uses curly brackets for the code itself, once the condition is satisfied.

NOTE #2: To make sure the code runs smoothly, you have to save the file using (cmd + s) to keep everything up to date. Then run the code.

For next week: Create a simple program using all of the types I have learned and conditionals


### 11/10/25
* I focused on creating multiple conditionals that would print simple statements:
    * ``` Swift
        let num = 17
        if num == 17 {
            print("num is 17")
        }

        let boo: Bool = true
        if boo == true{
            print("Let's GOOOO")
        }
      ```
* I moved on and watched video #3 of the [Swift tutorial](https://www.youtube.com/playlist?list=PLwvDm4VfkdpiLvzZFJI6rVIBtdolrJBVB) I found in the earlier weeks
    * Functions had a similar syntax as JavaScript with the exception that you use `func` to declare a function instead of `function`
* I created a function that had a print statement in it. I called the functions afterward:

``` Swift
func myFirstFunction(){
    print("Hello World")
}

myFirstFunction()
```
* I tried to call a function inside of a function:
``` Swift

func myFirstFunction(){
    print("Hello World")
    mySecondFunction()
}

func mySecondFunction(){
    print("My name is Joe")
}

myFirstFunction()
```

NOTE: Since `myFirstFunction` includes `mySecondFunction()`, whenever the function is called it prints both "Hello World" and `mySecondFunction`

* I added my first parameters into a function to then print out a statement using the arguments I used:

``` Swift
func myBio (name: String, age: Int){
    print("Hi, \(name)! You are \(age) years old.")
}
myBio(name: "Joe", age: 17)
```
NOTE: To use the values of the parameters, you have to put a `\` before `(parameter)`. This is called interpolation.
For for next time: Continue to learn more concepts and creating another simple program



### 11/23/25
* I focused on optionals this week, following video 6 of the [Swift playlist](https://www.youtube.com/watch?v=PDWNf4pBI64&list=PLwvDm4VfkdpiLvzZFJI6rVIBtdolrJBVB&index=7) as a guide
* I created my first optional variable and set it to three different values: `true`, `false`, `nil`
``` Swift
var numOne: Bool? = true
var numTwo: Bool? = false
var numThree: Bool? = nil
```

NOTE: Essentially, the three variables have this pseudo meaning: if there is a value, then it has to be a boolean. `nil` is a blank value that is similar to `null`. In conditions, `nil` acts as a false.

* I created a new optional variable and set it to `numThree`. I created another variable that was declared as a boolean and also set it to `numThree`:
``` Swift
var numFour: Bool? = numThree
var numFive: Bool = numThree // error
```
NOTE: In this case, `numFive` cannot be assigned to `numThree` because a non-optional variable cannot equal to an optional one.

* I assigned two question marks to and a `false` to my previous code for `numFive`:
``` Swift
var numFive: Bool = numThree ?? true
```

NOTE: In the code above, if there is a value for `numThree`, `numFive` will equal to `numThree`. Otherwise, it would be false. `??` is a nil-coalescing operator that means otherwise. If the first condition is not satisfied, the second one runs.

NOTE #2: Optionals are important because it avoids crashes. For instance, if a user types something, but there is no result, an optional variable saves the system from crashing.

For next time: Review more concepts, specifically Structs


### 12/1/25
* This week I focused on Structs. I referred to two videos in my [Swift playlist](https://www.youtube.com/watch?v=PDWNf4pBI64&list=PLwvDm4VfkdpiLvzZFJI6rVIBtdolrJBVB&index=7), that went over the topics, as a guide.
* First, I created my first struct:

```Swift
struct Book {
    let title: String
    let date: Date
}


let firstQuiz: Book = Book(title: "Quiz 2" date: Date())
```

NOTE: A struct is like a class in Java. You create what a struct should contain and then you can create "objects" of it.

* Next, I created an initializer inside the struct I had already created.

``` Swift
init(title: String, date: Date){
    self.title = title
    self.date = date
}
```
NOTE: `self` is a way to gather the instance variable of the class, similar to `this` in Java. In addition, the initalizer has the same function as `let firstQuiz: Quiz = Quiz(title: "Quiz 2" date: Date())`. But, it is more customizable to respond and fit the values of what a user would put.

* I created another initalizer within the same struct. But this time, I set `date` with a default value.

``` Swift
init(title: String, date: Date = .now){
    self.title = title
    self.date = date
}
```
NOTE: In case a user only puts in a string value, `date` would always have a default value of `.now`, or the current time. Like in Java, the constructor can have multiple parameters to account for every possibility of user input.

* At last, I created an immuatable struct, which contained variables that were delared with `let`.

```Swift
struct yourModel {
    let name: String
    let isCool: Bool
}
```

NOTE: When this struct is called, `name` and `isCool` is set to their apporiate value types by the user's input. After that, it is no longer able to be changed.

For next time: Focus on the concept of Tuples

### 12/8/25
* For this week, I focused on Tuples, following a dedicated [video](https://www.youtube.com/watch?v=zsjCrtENsZA&list=PLwvDm4VfkdpiLvzZFJI6rVIBtdolrJBVB&index=8) in the playlist I followed

NOTE: Tuples returns multiple values instead of just one thing

* I created my first Tuple:

```Swift
var myName: String = "Joe"
var userIsCool: Bool = false

func getUserName() -> String {
    myName
}

func getUserStatus() -> Bool {
     return userIsCool
}

func getUserInfo() -> (String, Bool){
    let name = getUserName()
    let status = getUserStatus()

    return(name, status)
}
```
NOTE: In the example above, I created two functions `getUserName` and `getUserStatus` to return the values of `myName` and `userIsCool`. Then, I set each values to `name` and `status` in a new function, `getUserInfo`, and returned both of the values as allowed by `(String, Bool)`.

NOTE: You do not need the `return` statement to return a value in a `func`, as shown in the `getUserName` function above.

* I created my first tuple variable of two data types: String and Bool.

```Swift
var userData: (String, Bool) = (myName, userIsCool)
```
NOTE: This variable will contain the values of `myName` and `userIsCool`. When it is printed, it will display `"Joe", false`.

* I created two additional variables to access information from my `getUserInfo` function.

```Swift
let infoOne = getUserInfo()
let dataOne: String = info1.0
```
NOTE: `dataOne` is of the string data type. The `.0` is similar to the concept of arrays. It points to the first value that the function returns, and it is based on zero-index counting.

For next time: Focus on using classes and accessing control

### 1/5/26
*  I continued to look over classes and access control after the break

* I created another class called firstClass and declared two new string variables: `title` and `name`. I also created an `init` and accepted tow parameters before setting `title` and `name` to them.
``` Swift
class firstClass {
    let title: String
    let name: String

    init(title: String, name: String){
        self.title = title
        self.name = name
    }
}
```
NOTE: Classes are slow because they are stored in heap. Structs on the other hand are fast because they are stored in the stack.

* Afterward, I created my first `deinit` within the class to destroy an object stored in memory.

```Swift
    deinit(){
        print ("Object is being deinitialized!")
    }
```

* I also added a function into the class to modify `title` and `name`.

```Swift
func modifyVal (newName: String, newTitle: String){
    self.name = newName
    self.title = newTitle
}
```
* In a new file, I created a public and private variable. I also printed both variables out.
```Swift
public var nameOne: String = "Joe"
private var nameTwo: String = "Joe Zheng"

print(nameOne)
print(nameTwo)
```
NOTE: In the example above, the second print statement would display an error. The concept of public and private is similar to Java. Public allows any other modules (apps/frameworks) to access the content. On the other hand, private only restricts access to the enclosing declaration, which can be classes, structs, or enums.

For next week: Focus on how to create algorithms with loops and arrays


<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
