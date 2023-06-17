# Clean Code

This repository presents the notes I made while reading the book
Clean Code from Robert C. Martin.

I've also extracted a few paragraphs and code snippets which I found to be important.

## Chapter 1 - Clean Code

### The Total Cost of Owning a Mess

__WIP__ Add Image here

### The Primal Conundrum

"Programers face a conundrum of basic values. All developers with more than
a few years experience know that previous messes slow them down. And yet
all developers feel the pressure to make messes in order to meet deadlines.
In short, they don't take the time to go fast!

True professionals know that the second part of the conundrum is wrong.
You will not make the deadline by making the mess. Indeed, the mess will
slow you down instantly, and will force you to miss the deadline. The only
way to make the deadline - the only was to go fast is to keep the code as
clean as possible all the times."

### What is Clean Code?

- Clean Code does one thing well.
- Clean Code reads like well-written prose.
- Clean Code is easily enhanced by others.
- Clean Code is surrounded by tests.
- Clean Code looks like it was written by someone who cares.
- Clean Code contains no duplications.

### We Are Authors

`@author`

Remember this when witting your code. You are not getting things done, but
also writhing for you and other people to read it later. We spend the majority
of our time reading code rather than writing it. By making code easy to read
we make it easy to write.

### The Boy Scout Rule

"Leave the campground cleaner than you found it."

"Always commit a cleaner code than what you initially pulled in. At the end of each day,
every small refactoring counts." _- Lucas Fabre_

## Chapter 2 - Meaningful Names

Choosing good names takes time but saves more than it takes.it takes.

- A good name should easily reveal the intent of a method.
- Avoid leaving false clues that obscure the meaning of code.
- When variables are used for different purposes give thm a good name distinction.
- Use pronounceable names.
  - Avoid names like `DtaRecrd` or `CtrlUsr`
- Use searchable names
- Avoid name prefixes.
  - `strPhoneString`
  - `ISomeInterface`
- Clarity is King.
- Class Names should be noun or noun phrase names.
- Method Names should have verb or verb phrase names.
- Choose clarity over entertainment.
- Pick one word per concept.
- Use Solution Domain Names
  - Prefer to use technical names.
- Use Problem Domain Names
- Provide the appropriate context when naming new items.

### Use Intention-Reveling Names

A good name should easily reveal the intent of a method. 

"The name of a variable, function or class should answer all the big questions.
It should tell you why it exists , what it does, and how it is used. If a name
requires a comment, then the name does not reveal its intent."

```java
int d; // elapsed time in days
int elapsedTimeInDays;
```

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
    if (cell.isFlagged())
      flaggedCells.add(cell);
  return flaggedCells;
}
```

### Avoid Disinformation

"...avoid leaving false clues that obscure the meaning of code."

- I.e. do not refer to a grouping of accounts as `accountsList`, unless it is really a list.
- Spelling similar concepts similarly is information. Using inconsistent spellings is disinformation.
  - `XYZControllerForEfficientHandlingOfStrings`
  - `XYZControllerForEfficientStorageOfStrings`

### Make Meaningful Distinctions

When variables are used for different purposes, give them a good name
distinctions such a way that others can easily understand the difference.

```java
public static void copyChars(char a1[], char a2[]) {
  for (let i = 0; i < a1.length; i++) {
    a2[i] = a1[i];
  }
}
```

```java
public static void copyChars(char source[], char destination[]) {
  for (let i = 0; i < source.length; i++) {
    destination[i] = source[i];
  }
}
```

### Avoid Mental Mappings

"Readers shouldn't have to translate a name into other names they already know."

"One difference between smart programmer and professional programmer is that the professional understands that _Clarity is King_. professionals use their powers for good and write code that others can understand."
