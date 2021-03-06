### Development

#### Top-down, what-if development
You want to write code from the top down. You start with the highest level code. Those one or two lines of code that will make everything work. Then you write what you would want and write your code that way. Because you are going top down, you're creating objects that don't exist and calling nonexistent methods on them. Doing this lets you define the usage before building the thing. Then you go down a level and repeat this process.

#### Your code as a product
You want to think of the methods you write, the objects you create, the APIs you design, and everything else as a product. Even if it's just you using it, imagine someone else will use it. This will lead to question such as
- Does this name make sense? Or is it obvious?
- How much work is it to use this? Am I creating an unnecessary burden on the user? Could I make this easier to use?
- How would someone *want* this to work? Does it work the way they would want it? Can I move this a step further in that direction?

#### Build out the critical paths first
By building out all of the critical paths of a feature first, you quickly resolve the unknowns and get a good idea of what is left to be done. 

#### Visualizing code
Visualizing code will lead you to better insights. Think of objects as visual components in your mind. Think of dependencies as wires between these boxes. Having public methods on an object is equiavalent to having buttons and levers on the object. Thinking this way, you see why minimizing the number of public methods reduces the complexity of a system.

#### Integration testing down to unit testing
You start with integration tests to define the high level outside behavior. When you find yourself testing too many cases and it becomes too tedious to write these tests, you drop down one level into the unit test and test all of the details there.

### Problem Solving
####Has this problem been solved already?

####Is there a related or equivalent problem that will lead me to a solution?

Ex 1: A solution to the problem in a different language.

Ex 2: Performing a hit test--knowing if you clicked on something--is the same as knowing if a point is inside of a polygon.

####Is there a solved problem that could contain my solution?

Ex 1: Look at another ember addon to see how they do configuration

Ex 2: Look at an e-commerce platform to figure out a good database architecture for your custom e-commerce site

Ex 3: You want to figure out how to do collision detection, so you look for an open source video game to see how they do it.

Ex 4: I want to keep track of which routes get hit in an Ember application. If you look for how to track page views using an analytics library, that will contain your solution. This is because in order to track page views, you probably need to be able to hook into when a route is hit.

####Can I break this problem down into smaller problems?

####Can I exaggerate the problem or make it more obvious?

Ex 1: If you are writing a method to shrink an image to fit in a bounding box, and the ratios aren’t working properly, exaggerate the ratios. Pick ratios like 100 by 5.

Ex 2: If there is a layout issue on your HTML page, add a red outline to all the elements.

Ex 3: If you suspect a timing issue, add an intentional delay to check your assumption.

####Are there things where, if they existed, they would help you solve the problem?
_I call this "if-only" thinking or "wishful" thinking_

Ex 1: If only you could break on XHR requests, it would make your life easier. Then you can research to see if something like this exists.

Ex 2: If only bower let me develop addons locally, it would speed up my development time. Then you can research to see if this option exists.

### Prioritizing
When working on a feature, the order you work on things matter. Think of a feature as a goal that a user wants to accomplish. A feature where a merchant can list products on a store has the final goal of a listed product with all of the proper attributes. Knowing this, here are the guidelines of prioritizing

- Show Stoppers: Anything that makes it impossible to accomplish the goal goes first.
- Major Annoyances: Things that really damage the user experience. Example would be that they have to refresh the page to see their changes. Generally can go from most major annoyance to least major annoyance.
- Major Refactoring: If there are things that are really getting in the way of changing code, this is the time to refactor. Don't refactor 100% at this point. Just clean up what is getting in your way.
- Minor Annoyances: Things that hurt the user experience but the person can get over. Example would be an error message popping up in the middle but if they hit ok they can keep going
- Minor Refactoring

### Should I make my code more general?
Sometimes we consider adding more flexibility to our current code in order to make future changes easier or to make a piece of code usable for some slightly different scenarios. This process has a couple issues:

-  **The extra code you write may not be used at all.**
The other scenarios where the code piece will be needed may never come, but you may have spent 4 more hours trying to make your code work for all future scenarios that will not exist.

- **You may lose a lot more time on a task that shouldnt normally take that long.**
    Yeah, of course this is ususally answered with the "I'm saving a lot of time for later" response, but you never know the actual amount of time you're saving for the future. If you need to do something ASAP, dont waste time today to save you some unknown time tomorrow.

- **You may not be aware of what things need to be common between scenarios.**
    Writing code for one scenario may not give you enough information about the common things among all the future scenarios. Usually the magic number of cases is 3, after you copy and modify a piece of code for the third time you should know in that moment what needs to be in all scenarios and extract that in a class or any other extensible code statement.

#### When to generalize:

The 3 cases rule mentioned before is very useful for this, if you have more than 2 cases where a piece of code is repeated, you should have a pretty accurate idea of what needs to be generalized and how to do it.

There are some cases when generalizing right away may be worth it. There's a couple questions you can ask yourself to identify them:

- How much work will it be to generalize this code now?
- How much work will it be to generalize this code when I need it to handle other cases?

If generalizing later will increase the overall work by a lot, then you should generalize it right away.

### Skills and principles for becoming a great developer
- Wishful thinking
  - APIs, classes, methods, implementation
  - Development tools
  - Paying attention to your wishes
- Separating "what do I want?" from "how can I do this?"
- How what, why, and how are connected. (Why is a level up the layer of abstraction, what is the current level of abstraction, how is one level down of abstraction. See tree mental model.)
- Top-down thinking
- Simplifying a problem
- Root cause analysis of a problem
- Understanding a problem with examples
- Breaking a problem into sub-problems
- Prioritizing the order of implementation
- Naming things
- Empathy when writing code. Thinking about someone else reading, modifying, and using it.
- Solution finding
  - Problem finding
  - Problem equivalence (if I know how to find X, then I'll know how to solve Y)
  - Solution finding
  - Using Google
  - Within the same project
  - Text search techniques
  - Following a loose trail 
- Debugging
  - The factory technique
  - Simplifying the bug
  - Making and testing hypothesis
  - The difference technique
  - Linear vs. exponential elimination 
  - Improving the feedback loop
- Mental models
  - Code as a machine
  - Visualizing dependencies
  - Objects as people in an organization
  - Imaginary friend
  - Tree of abstraction
- Doing things consciously
- Why you usually get stuck (you are at the wrong level of abstraction)
- Reflection process
  - Is there a general principle here?
  - How can I do this better the next time?
  - What did I do wrong?
  - What did I do right?
- Communicating to a the non-technical person
  - Understanding the information they need and don't need
  - Clarifying requirements with the use of examples
  - Asking why to uncover better solutions
