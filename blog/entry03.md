# Entry 3
##### 2/2/26

### Context
Following the winter break, I continued to watch through the [Swift tutorial playlist](https://www.youtube.com/playlist?list=PLwvDm4VfkdpiLvzZFJI6rVIBtdolrJBVB) I found to learn new concepts. Previously, I learned about the different types of Swift variables and loops. But over the past few weeks, I focused on the core concepts of access and control, knowing that they would be extremely vital in my brain stimulating app as I work between different pages.

To begin with my tinkering process, I first created a new class called `firstClass` and within it, I created two variables of the `String` type: `title` and `name`. After that, I created an `init`, which is essentially the equivalent of a constructor in a Java class, and gave it two parameters: `title` and `name` respectively. I also made parameters the `String` data type.

``` Swift
class firstClass {
    let title: String
    let name: String
```
Within the `init`, I used the `self` keyword to call the instance variables. I added `self.title = title` and `self.name = name` to change the instance variables to the values of the parameters.

``` Swift
init(title: String, name: String){
        self.title = title
        self.name = name
    }
```

Next, I created my first `deinit` within the class to destroy an object stored in memory. Within the `deinit`, I added a `print` statement to display the following phrase: "Object is being deinitialized". I also created another function called `modifyVal` to modify `name` and `title`, which is initialized by the `init`. Like the code process in the `init`, I added `self.title = title` and `self.name = name`. In the end, I created two new instance `String` variables: nameOne and nameTwo. But this time, one was public and the other private. I printed them out in the end:

```Swift

public var nameOne: String = "Joe"
private var nameTwo: String = "Joe Zheng"

deinit(){
        print ("Object is being deinitialized!")
    }

print(nameOne)
print(nameTwo)
```

As of recently, I have also downloaded Xcode. I plan to familiarize myself with the coding platform and transition to it fully from VScode since it is the best supported Swift program. Concept wise, I will learn how to build a main page of my Brain Stimulating App.

### EDP
As of right now, I am on stages three and four in the Engineering Design Process: Brainstorm possible solutions and Plan the promising solutions. Now that me and Kyle have identified a clear problem, we hope to tackle it by creating an app. But in order to maximize our solution effect, we need to understand which features to add in our apps.

### Skills
#### Organization
As I was tinkering, I organized my files on VSCode and also keep track of my to-do list to ensure I can learn Swift effectively. Taking notes was important, but getting on top of myself and knowing where everything I need is allowed me to learn with less complication. Not only that, but I could refer back to any interesting code I saved to process it. 


#### Decision-Making
After much tinkering on VSCode, I have made the decision to swap over to Xcode. I felt ready to make the switch as I believed I gained enough knowledge to start a tiny draft on my solution. But I also believe that decision-making is especially important during this project. I have to understand when it is the right time to adjust to get the best outcomes.



[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
