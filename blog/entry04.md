# Entry 4
##### 3/9/26

### Context
Since the last blog, I have created my [MVP plan](https://github.com/kylel5957/apcsa-freedom-project/blob/main/prep/plan.md), listing out every step I need to take to create my envisioned prototype of a brain stimulating app. I've set appropriate deadlines that complemented with my schedule. Afterward, I followed my plan accordingly, making necessary features of my app on Xcode to meet the requirements that I established for myself. For any new concept that I came across during my tinerking process, I also jotted them in my [learning log](../tool/learning-log.md).

### Tinkering
To begin with my tinkering process, I created a new project folder called mentalwellness to store all of my Swift files. Within the folder, I first navigated to `ContentView`, which was the main page.

I intended to add three options on the main page: play, settings, and resources. The play button will bring users into a catalog of games. The settings gives users the ability to make any necessary changes on their devices. The resources section will provide users with statistics relating to their cognitive test results.

Adding onto the starter code, I included `NavigationLink()` three times, one for each section I wanted to add. Within the first `NavigationLink()`, I set the name equal to Start, and then I linked its `destination:` to `Start()`. I also included a `.buttonStyle(.borderedProminent)` to display the button itself. I repeated the same process, naming the next two `NavigationLink()` Settings and Resources and directing their `destination:` to `Settings()` and `Resources()`.
``` Swift
 NavigationLink("Start", destination: Start())
    .buttonStyle(.borderedProminent)

 NavigationLink("Settings", destination: Settings())
    .buttonStyle(.bordered)

 NavigationLink("Resources", destination: Resources())
    .buttonStyle(.bordered)
```

After setting up the `NavigationLink()` on the main page, I  created additional files to ensure that each `destination:` had a pathway. I named the files as `Start.swfit`, `Resources.swift`, and `Settings.swift`. In all of the files, I added a `Text()` and included a title within the parenthesis. I also changed the font appearance by using `.font(title)` and `.bold()`.

```Swift
// Start.swift file
VStack {
            Text("Game Menu")
                .font(.title)
                .bold()
        }

// Resources.swift file
VStack {
            Text("Resources Screen")
                .font(.title)
                .bold()
        }

// Settings.swift file
VStack {
            Text("Settings Screen")
                .font(.title)
                .bold()
        }
```


Over the next few weeks, I am creating multiple games and linking them to pages, which can be navigated through the `play` section.

### EDP
As of right now, I am on the fifth stage of the Engineering Design Process: Create a prototype. After learning and tinkering with Swift over the past few of weeks, seeing which concepts are important for my solution, I am finally starting to create what I entailed at the start of the year. In the next few weeks, I will work with Kyle, following the MVP plan to create a minimal viable product before making additional changes for refinery purposes.

### Skills
#### How To Research
While I tinkered with many concepts throughout the [tutorial videos](https://www.youtube.com/playlist?list=PLwvDm4VfkdpiLvzZFJI6rVIBtdolrJBVB) I watched, some weren't directly applicable with creating a menu. Instead, there were additional lines of code that was directly meant to create a main page. Because of this, I had to conduct additional research, searching phrases such as "Essential components needed to create a main menu page on Swift". Through this, I was able to work effectively and construct a menu in a relatively quick time with little to zero difficulties.

#### Time Management
Now that it is time to create a prototype to solve our discovered issue, we have to follow a schedule to ensure  everything is completed on time. I have to be decisive and be certain of my intended actions, weighing theirs pros of cons in order to reach my intended goal of creating a brain stimulating app that works to improve the activeness of cognitive functions in people.
[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
