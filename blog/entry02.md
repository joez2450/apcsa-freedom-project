# Entry 2
##### 12/15/25

### Context
For the past few weeks, I continued to tinker with Swift, an IOS development tool that I selected to build my Freedom Project idea of creating a brain stimulating app.

### Tinkering
So far, I have learned four topics: Structs, Tuples, and Functions, using a [Swift tutorial](https://www.youtube.com/playlist?list=PLwvDm4VfkdpiLvzZFJI6rVIBtdolrJBVB) as a reference to guide along the way.

First, I tackled functions. I created a new `func` and called it `myFirstFunction`. Within it, I added a `print` statement to output "Hello World".

``` Swift
func myFirstFunction(){
    print("Hello World")
}
```

I also created a new `func` and named it `myBio`. I added two parameters `name: String, age: Int` which took two data inputs from the users, a String and an Int. Next, I added a `print()` with `"Hi, \(name)! You are \(age) years old."` inside of the parenthesis, so it would greet the user and tell them the age after the `func` was called.

``` Swift
func myBio (name: String, age: Int){
    print("Hi, \(name)! You are \(age) years old.")
}
myBio(name: "Joe", age: 17)
```

After that, I moved onto Structs, which was essentially a class in Java. You can create a struct and create "objects" of it. I declared a `struct` and named it Book and put an opening and closing bracket. Afterwards, I declared two variables using `let` and named them `title` and `date`. For title, I set the data type to `String`. For date, I set it to `Date`.

```Swift
struct Book {
    let title: String
    let date: Date
}
```

At last, I created a tuple, which is used to return multiple values instead of one in a function. I created two functions `getUserName` and `getUserStatus` and set them to return a `String` and `Bool` respectively. Next, I created two variables: `var myName: String = "Joe"` and `var userIsCool: Bool = false`. Inside the parenthesis of `getUserName`, I returned `myName`. In `getUserStatus`, I returned `userIsCool`.

```Swift
var myName: String = "Joe"
var userIsCool: Bool = false

func getUserName() -> String {
    myName
}

func getUserStatus() -> Bool {
     return userIsCool
}
```

I created one last `func` and named it to `getUserInfo`. This time, I set the function to return a `(String, Bool)`. Within the function itself, I let `name = getUserName()` and `status = getUserStatus()`. I added a return statement and placed `name` before `status` to fit the `(String, Bool)` requirement.

```Swift
func getUserInfo() -> (String, Bool){
    let name = getUserName()
    let status = getUserStatus()

    return(name, status)
}
```

During the break, I will focus on the topics of using classes and accessing control by watching the tutorial videos in the Swift playlist I found.

### Engineering Design Process
As of right now, I am on the second stage of the Engineering Design Process: Research the problem. I have already defined a problem to tackle with Kyle, which was to improve brain functions against factors such as old age and social media addiction. I will need to conduct more research on my issue and then find ways to resolve it using Swift.

### Skills
#### Effectively Using Resources
Throughout my tinkering process, I had mainly followed one Swift tutorial playlist on YouTube. While the videos were in-depth, it was also very long if I had watched every second. To be more effective with my time, I played the video in 2x speed and also skipped any parts that seemed simple and basic. In addition to that, I also looked at the bookmarks provided by the video creater and see which topics would be most relevant to my creation as I start to brainstorm solutions to my problem. 

#### Organization
Starting to learn a new tool is difficult as it requires you to learn many concepts and components. But, I have created bookmarks to the resources I have been using frequently to learn. By doing this, I stay organized and also get to the places where I want to be at a quicker speed. Not only that, but it also allows me to conduct more tinkering process without having to be stuck and figuring out where certain links or files are at.

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
