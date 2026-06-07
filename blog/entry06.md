# Entry 6
##### 5/8/26

### Context
Ever since the last blog, I have been refining my app by implementing Beyond MVP features. After engaging in a gallery walk activity, I was able to receive feedback from my peers, and comparing their answers with the ones that Kyle recieved, we found three main points to work on in our game: improve the asthetics of our app, add a settings option to change the background color, and provide a FAQ section. As we pinpointed these, I immediately got to work and browsed [W3schools](https://www.w3schools.com/swift/swift_ui_styling_theming.asp) and watched a [YouTube tutorial](https://www.youtube.com/watch?v=JqQQozkFeJU) to understand how I can bring these suggestions to my app.


### Process
In Xcode, I started off by with a transition to using `TabView` and `Tab` to change the overall design of the user interface. While `NavigationStack` was a viable option, having multiple padded out buttons as a main menu lacked asthetics. `Tab` provided a more cleaner and organized look. I replaced the `NavigationStack` and `NavigationLink` within my main code file with `TabView` and `Tab`. Within each `Tab`, I gave it a distinct name (i.e. resources, home), and I also included an embedded `systemImage` so that each tab would have an appropriate display icon. Ultimately, my code looked like this:


```Swift
      TabView{
                    Tab("Home", systemImage: "play.circle"){
                        Text("Home")
                        ScrollView{
                            LazyVStack(spacing: 12){
                                GameCard(title: "Reaction Time Test", description: "Quiet your thoughts to sharpen your senses. A calm mind is the fastest to move.", iconName: "brain", destination: GameSceneOne())
                                GameCard(title: "Brain Coordination", description: "Clear your sight and calm your pulse. Accuracy flows from a centered mind.", iconName: "scope", destination: GameSceneTwo())
                                GameCard(title: "Memory Test Game", description: "Flip, focus, and find the pair. Strengthening your memory starts with being fully present.", iconName: "timer", destination: GameSceneThree())
                            }
                            .background(LinearGradient(colors: [.blue, .green], startPoint: .top, endPoint: .bottom))
                            .ignoresSafeArea()
                        }
                        .scrollContentBackground(.hidden)
                    }
                    Tab("Resources", systemImage: "star.fill"){
                    }
                }
```

For my settings page, I included it in my `Resources` tab. After researching different code syntaxes on W3schools, I found `DisclosureGroup()` to be the most effective for my goal of creating an FAQ page as it served similarly to a dropdown menu. Within the parenthesis, you would include your question, and within the opening and closing brackets, there will be a `Text` that includes the answer.

In my case, I decided to add 3 important questions, which focused on our aim of reducing social media addiction, and their answers. Accordingly, I created three different `DisclosureGroup()` and using `Text`, I added their respective answers. Because everything was tightly packed, I added padding to create more spacing around each box, making my final code look like this.

```Swift
                        DisclosureGroup("What is the mission of the game?") {
                                   Text("This game aims to stimulate well-being and the start of healthier habits. Rather than having online competition, we made it  solitary, and the only goal is to improve yourself. Having no distracting noises or elements, our goal was to provide a space where positive resources and small games can intersect.")
                               }
                               .padding()
                        DisclosureGroup("How can I start to use less social media?") {
                                   Text("Start by being more mindful and set a goal of what you want to achieve when you get online. Rather than constantly scrolling, do what you have to do and get back offline. Additionally, to supplement this process, you can turn off notifications and set a goal of a certain period of time to get off social media (1 day, 3 days, 1 week, etc).")
                               }
                               .padding()
                        DisclosureGroup("How can I get involved to become more mindful?") {
                                   Text("Check out communities like Internet and Technology Addicts Anonymous (ITAA) and Media Addicts Anonymous (MAA) as they provide meetings and tools for reducing social media usage. Tools such as Screen Time (IOS) or Digital Wellbeing (Android) monitor screen time and are a great resource in seeing where to start.")
                               }
                               .padding()
```

Finally, I focused on creating a skider that would change the background color of my app. I wanted to keep things simple, so I focused on creating a light and dark mode feature. For this feature of my app, I used a `Toggle()`, where within the parenthesis, I added the title "Dark Mode" and a boolean status to see if the mode is on: `isOn: $isDark`. Then, I used `preferredColorScheme(isDark ? .dark : .light)` so that if `isDark` is true, then the color scheme will be dark. Otherwise, it would change to be light.

### EDP
Currently, I have completed stage 7 of the Engineering Design Process, which is to improve my prototype as needed. I am still working on stage 8, where I need to communicate my results. So far, I have already created slides and presented in class as well as the SEP Expo. However, because I was also selected as a showcase finalist with Kyle, we are both working to deliver a presentation that is shortly coming up.

### Skills
#### Time Management
Because it is June, all of the final exams and presentations are happening at once. To prepare for the Expo, I had to communicate clearly with my partner Kyle while also regularly adapting my schedule to ensure that I could complete my work alongside little to no conflict from the other competitions I was involved in. Not only that, since our coding project was also extremely complex, it also meant that it would take longer to break down the code into easy information for the audience to digest. To combat this, we would also work ahead of time to leave buffer time for possible revamps later on.

#### Organization
While making the presentations, I had to get hold of all of my coding files while also searching for reliable data to hook the audience in. Since there were a lot of different materials to manage, I usually create dedicated folders or leave specific notes detailing my plans on how to utilize the resource. Because of this, I rarely struggled with mental clarity and unnecessary stress while figuring out the next step. Such techniques only boosted my working efficiency, and I was able to utilize my time better admist a very busy academic season.


[Previous](entry05.md) | [Next](entry07.md)

[Home](../README.md)
