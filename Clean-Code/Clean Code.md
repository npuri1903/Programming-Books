# Clean Code
## Clean Code

### There Will Be Code
There will always be code, no matter how much higher level it can get. We can write tools that write code for us. But they have to be provided with a specification. That specification is code.

### What is Clean Code?
>I like me code to be elegant and efficient. The logic should be straightforward to make it hard for bugs to hide, the dependencies minimal to ease maintenance, error handling complete according to an articulated strategy, and performance close to optimal so as not to tempt people to make the code messy with unprincipled optimizations. Clean code does one thing well.

**- Bjarne Stroustrup, inventor of C++ and author of The C++ Programming Language.**


> Clean code is simple and direct. Clean code reads like a well=written prose. Clean code never obscures the designer’s intent but rather is full of crisp abstractions and straightforward lines of control.

**- Grady Booch, author of Object Oriented Analysis and Design with Applications**


> I could list all of the qualities that I notice in clean code, but there is one overarching quality that leads to all of them. Clean code always looks like it was written by someone who cares. There is nothing obvious that you can do to make it better. All of those things were thought about by the code’s author, and if you try to imagine improvements, you’re led back to where you are, sitting in appreciation of the code someone left for you - code left by someone who cares deeply about the craft.

**- Michael Feathers, author of Working Effectively with Legacy Code**


> You know you are working with clean code when each routine you read turns out to be exactly what you expected. You can call it beautiful code when the code also makes it look like the language was made for the problem.

**- Ward Cunningham, inventor of Wiki inventor of Fit, co-inventor of eXtreme Programming. Motive force behind Design Patterns, Smalltalk and OO thought leader. The godfather of all those who care about code.**


### We Are Authors
And we have readers. So write your code thinking about the reader. Making code easy to read actually makes it easier to write.


### The Boy Scout Rule
Leave the campground cleaner than you found it.


## Meaningful Names
![Image of children neading a name.](http://www.javaskool.com/codeResources/CleanCodeChapters/cleancodePics/meaningfulNames.png)
Names are everywhere in software. We name our variables, functions, arguments, classes and packages. We name our source files and the directories that contain them. We name our jar files and war files and ear files. Because we do so much of it, we’d better do it well.

### Use Intention-Revealing Names
We are serious about it.

```
int d; // elapsed time in days
int elapsedTimeInDays;
```

```
public List<int[]> getThem() {
    List<int[]> list1 = new ArrayList<int[]>();
    for(int[] x : theList)
        if(x[0] == 4)
            list1.add(x);
    return list1;
}

public List<int[]> getFlaggedCells() {
    List<int[]> flaggedCells = new ArrayList<int[]>();
    for(int[] cell : gameBoard)
        if(cell[STATUS_VALUE] == FLAGGED)
            flaggedCells.add(cell);
    return flaggedCells;
}

public List<Cell> getFlaggedCells() {
    List<Cell> flaggedCells = new ArrayList<Cell>();
    for(Cell cell : gameBoard)
        if(cell.isFlagged())
            flaggedCells.add(cell);
    return flaggedCells;
}
```

### Avoid Disambiguation
Do not refer to a grouping of accounts as an `accountList` unless it's actually a List.

Beware of using names which vary in small ways. How long does it take to spot the subtle difference between a `XYZControllerForEfficientHandlingOfStrings` in one module and, somewhere a little more distant, `XYZControllerForEfficientStorageOfStrings`? 


### Make Meaningful Distinctions
```
getActiveAccount();
getActiveAccounts();
getActiveAccountsInfo();
```

### Use Pronounceable Names
If you can't pronounce it you can't discuss it without sounding like an idiout. "Well, over here on the bee cee arr three cee enn tee we have a pee ess zee kyew int, see?"

### Use Searchable Names
The length of a name should correspond to the size of its scope.

### Avoid Encodings

### Hungarian Notation
Not required anymore.

### Member Prefixes
Not required anymore, just adds up to the clutter. You sould be using a programming environment that highlights or colorizes members to make them distinct.

### Interfaces and Implementations
These are sometimes special case for encodings. Avoid using `I` for an interface, encode the implementation instead, i.e. instead of `IShapeFactory` implemented by `ShapeFactory`, use `ShapeFactory` implemented by `ShapeFactoryImpl`.

### Avoid Mental Mapping

### Class Names
Classes and objects sould have noun or noun phrase names like `Customer`, `WikiPage`, `Account` and `AddressParser`. Avoid words like `Manager`, `Processor`, `Data` or `Info` in the name of a class. A class name should not be a verb.

### Method Names

