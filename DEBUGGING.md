# Checklist for debugging the issue 

**Listed in rough order of importance**


## Simplify the problem relentlessly
- Comment out all unrelated code until the bug goes away
- Reduce the number of moving parts (hardcode variables, etc)
- Disable libraries

## Understand the problem
- Get to the root cause by asking "why" repeatedly
- Understand when the problem occurs and when it doesn't occur
- Search the codebase for all occurences of unique keywords to see all related areas of the code

## Search for related problems and solutions
- Your codebase
- Google
- Stack Overflow
- GitHub Issues
- Past experience

## Exaggerate the problem and make it more obvious
- Ex: If you are writing a method to shrink an image to fit in a bounding box, and the ratios aren’t working properly, exaggerate the ratios. Pick ratios like 100 by 5.
- Ex: If there is a layout issue on your HTML page, add a red outline to all the elements.
- Ex: If you suspect a timing issue, add an intentional delay to check your assumption.

## Tighten the feedback loop
- Conditional breakpoints so you don't have to hit next so many times
- Run an individual test instead of all of them
- Use the javascript console instead of modifying the code


## Guess and test
- If you suspect what the problem is, ask "what is the simplest way to test my theory?"
  - Add a debugger statement or conditional debugger statement
  - Raise an exception to see if a line is hit
  - Hardcode values
  
