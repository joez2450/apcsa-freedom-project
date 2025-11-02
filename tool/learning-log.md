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

* I created my first set of boolean variables
    *  ``` Swift
        let firstItem = true

        let firstItemOne: Bool = true
       ```
NOTE: In both cases, the variables are set to the value true. `:Bool` only declares the variable as a boolean type. The same can be applied to other types like strings.

* I tested out a new concept: `Date` type. I created a variable and set it equal to `:Date` type and `Date()`.
    * ``` Swift
        let myDate: Date = Date()
      ```

NOTE: The value of `Date()` is the current day, month, year, and time. It is considered right now.


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

For next week: Create a simple project using all of the types I have learned and conditionals
<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
