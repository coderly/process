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
- Major Annoyances: Things that really damage the user experience. Example would be that they have to refresh the page to see their changes.
- Major Refactoring: If there are things that are really getting in the way of changing code, this is the time to refactor. Don't refactor 100% at this point. Just clean up what is getting in your way.
- Minor Annoyances: Things that hurt the user experience but the person can get over. Example would be an error message popping up in the middle but if they hit ok they can keep going
- Minor Refactoring
