# Clean Code

This repository presents all the notes I made while reading the book
Clean Code from Robert C. Martin. I've also extracted a few paragraphs
which I found to be important.

## Chapter 1 - Clean Code

### The Total Cost of Owning a Mess

__WIP__ Add Image here

#### The Primal Conundrum

"You will not make the deadline by making the mess. Indeed, the mess will
slow you down instantly, and will force you to miss the deadline. The only
way to make the deadline - the only was to go fast is to keep the code as
clean as possible all the times."

### We Are Authors

@author

Remember this when witting your code. You are not getting things done, but
also writhing for you and other people to read it later.

"So if you want to go fast if you want to get done quickly, if you want
your code to be easy to write, make it easy to read."

### The Boy Scout Rule

"Leave the campground cleaner than you found it."

Checkout the code cleaner than you pulled it in. In the end of the day
every small refactor counts.

### What is Clean Code for you?

__WIP__ -

## Chapter 2 - Meaningful Names

### Use Intention-Reveling Names

"It is easy to say that names should reveal intent."

"Choosing good names takes time but it saves more than it takes."

"The name of a variable, function or class should answer all the big questions.
It should tell you why it exists , what it does, and how it is used. If a name
requires a comment, then the name does not reveal its intent."

```java
public List<int[]> getThem() {
  List<int[]> list1 = new ArrayList<int[]>();
  for (int[] x : theList)
    if (x[0] == 4)
      list1.add(x);
  return list1;
}
```

```java
public List<int[]> getFlaggedCells() {
  List<int[]> flaggedCells = new ArrayList<int[]>();
  for (int[] cell : gameBoard)
    if (cell[STATUS_VALUE] == FLAGGED)
      flaggedCells.add(cell);
  return flaggedCells;
}
```

### Avoid Disinformation

"...avoid leaving false clues that obscure the meaning of code."
