# Entry 5
##### 4/13/26

### Context
Ever since the last blog, I have followed my [MVP plan](https://github.com/kylel5957/apcsa-freedom-project/blob/main/prep/plan.md) and the deadlines I set for myself to build a minimal viable product that functioned. As I was constructing my prototype with Kyle, I also referred to various parts of a [Swift tutorial](https://www.youtube.com/watch?v=-VC3hIEL7eQ) to learn new code that were of immediate need to build certain features (navigation) that I desired. In addition, I used [W3Schools](https://www.w3schools.com/swift/) to learn any additional syntaxes and their function that seemed to be useful in my solution.

### Tinkering
Continuing with the same file where I made a main menu page using `NavigationLink` that allowed a user to travel multiple pages, I created my first game: Reaction Time Test. I began by creating six variables: `gameState = false`, `startTime = Date()`, `backgroundColor = Color.blue`, `message: String = "Click to start"`, and `isActive = false`. `gamestate` would check to see if the game is active. `startTime` stores the current time in the moment, which would be useful to calculate reaction time later on.

Next, I worked on creating a `check` function, whose purpose is to see the state of the game and update changes as needed. If `gameState` is true, and if `backgroundColor == .green` that would mean the game has to end when the user clicks the screen. Therefore, within the nested if statements, I added `EndGame()`. But if `backgroundColor` did not equal green, then a "Too soon!" message should logically appear. So in the nested `else` statement, I added `message = "Too soon!"`. If neither conditions were true, then the game has to start, calling `GameStart()` within the else statement.


```Swift
  func check(){
        if gameState {
            if backgroundColor == .green {
                EndGame();
            } else {
                message = "Too soon!"
            }
        } else { GameStart();
        }
    }
```

After that, I had to create the `GameStart(0)` function, which I defined in the `check()` function. The purpose of this function was to ensure the background starts at red and changes to green after a random time. First, I set `isActive` and `gameState` to true. In addition, I set `message` to "Wait for green...". The next step I took was setting the background color to red by setting `backgroundColor` to `Color.red`. For the random timer, I created a new variable `randomDelay` and set the value to `Double.random(in: 1.0...8.0)`, allowing the background to switch colors anywhere between 1 to 8 seconds. To ensure the UI runs after the delay occurs, I added `        DispatchQueue.main.asyncAfter(deadline: .now() + randomDelay) {`. In the end, I added a conditional to see if `isActive` is true, which if it was, then `backgroundColor` would be equal to `Color.green`, `message` hold the string "TAP!", and `startTime` will be updated to `Date()`.

```Swift
  func GameStart() {
        isActive = true;
        gameState = true;
        message = "Wait for green...";
        backgroundColor = Color.red;
        let randomDelay = Double.random(in: 1.0...8.0)
        DispatchQueue.main.asyncAfter(deadline: .now() + randomDelay) {
            if self.isActive {
                self.backgroundColor = Color.green;
                self.message = "TAP!";
                self.startTime = Date();
            }
        }
    }
```

Finally, I created one final function, which was `EndGame()`. This function had the task of displaying the reaction time and also changing the background color back to the default blue. Immeidately, I declared a new variable `timeTaken`. Because I needed the time it took for the user to click when the background turns green, I set `timeTaken` equal to `Date().timeIntervalSince(startTime)`. I also created a new variable `ms` so the final reaction time could be measured in milliseconds. For `ms`, I set the value equal to `(int)(timeTaken * 1000)`. And in the end, I set `message` equal to `"\(ms)ms\nTap to play again"`,`backgroundColor` to `Color.blue`, `isActive = false`, and `gameState = false`.

```Swift
func EndGame(){
        let timeTaken = Date().timeIntervalSince(startTime);
        let ms = Int(timeTaken * 1000);
        message = "\(ms)ms\nTap to play again";
        backgroundColor = Color.blue;
        isActive = false;
        gameState = false;
    }
```

In the main body, I included a NavigationStack and a VStack within it, where I put the title of the game and implemented a background color. I also added a `NavigationLink` to go back to the main menu, and a `.onTapGesture` that would activate the function `check()`.

```Swift
 NavigationStack {
            VStack {
                Text("Reaction Time Game")
                    .font(.title)
                    .bold()
                    .padding(.top)
                Text(message)
                    .font(.headline)

                backgroundColor
                    .ignoresSafeArea()
            }
            .onTapGesture{
                check();
            }
            NavigationLink("Return to Main Menu", destination: ContentView())
                .buttonStyle(.borderedProminent)
                .padding(.bottom)
        }
```


While I worked on the reaction time game, Kyle created an aim trainer game, helping with brain reflexes. For our beyond MVP, we will add additional games while also enhancing the main menu using `TabView` as we will primarily focus on developing an app dedicated for IOS.

### EDP
I am currently on both the fifth and sixth stages of the Engineering Design Process: Create a prototype and Test and evaluate the prototype. I have created a functional app with Kyle and during the process, we tested various features to everything ran the way we wanted it to be. In the coming weeks, we will head into making any beyond MVP changes to improve our solution app as needed. These include enhancing visuals and fixing game bugs.

### Skills
#### Organization
While coding in Xcode, I had many files that I had to name appropriately. This was because each file had their own purpose for my app. I needed to ensure that the file path was correct so it would minimize errors and reduce the likelihood of having to debug. In addition, I also had to keep track of all of the useful videos I found, usually putting the links into a separate doc that I could refer back to later.

#### Management
Because Kyle and I had set many expectations for our MVP, we needed to be able to manage the workload to achieve what we envisioned. Each game required many different concepts to be tied together so we had to conduct additional research to supplement the knowledge we already attained throughout the months leading up to now. Given how many different tasks we need to complete to reach our goals, we need to stay managed to
stay effective and efficient.

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
