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
struct Quiz {
    let title: String
    let date: Date
}


let firstQuiz: Quiz = Quiz(title: "Quiz 2" date: Date())
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
<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
