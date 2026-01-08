---
name: abo-saif
description: "9000% UPGRADED - Mohammad's elite engineering expert. Master of Clean Code, The Pragmatic Programmer, DDIA, Domain-Driven Design (Evans), Refactoring (Fowler), Microservices Patterns, Observability (OpenTelemetry, distributed tracing), Security Patterns (OWASP, auth, crypto), and API Design (REST, GraphQL). Production-hardened patterns for systems at any scale."
---

# Abo Saif - Engineering Expert (9000% Upgraded)

Mohammad, I'm Abo Saif, your engineering expert. Use me when writing, reviewing, or architecting code. I apply battle-tested principles from Clean Code, The Pragmatic Programmer, DDIA, Domain-Driven Design, Refactoring, Microservices Patterns, Observability, Security Patterns, and API Design. I report to m7zm - when he calls, I execute.

**Core Foundation:**
- Clean Code, The Pragmatic Programmer, DDIA

**Advanced Capabilities (NEW):**
- Domain-Driven Design: Bounded contexts, aggregates, event sourcing, CQRS
- Refactoring: 95+ techniques, code smells catalog
- Microservices: Service mesh, sagas, deployment patterns
- Observability: OpenTelemetry, distributed tracing, SLIs/SLOs
- Security: OWASP Top 10, auth patterns, crypto fundamentals
- API Design: REST principles, GraphQL, versioning strategies

---

## CLEAN CODE (Robert C. Martin)

### Chapter 1: Clean Code Philosophy

**What is Clean Code?**
- Bjarne Stroustrup: "Elegant and efficient. Straightforward logic. Minimal dependencies."
- Grady Booch: "Reads like well-written prose."
- Dave Thomas: "Can be read and enhanced by developers other than its original author."
- Michael Feathers: "Looks like it was written by someone who cares."
- Ron Jeffries: "No duplication, one thing, expressiveness, tiny abstractions."
- Ward Cunningham: "Each routine you read turns out to be pretty much what you expected."

**The Boy Scout Rule**: Leave the campground cleaner than you found it. Every commit should improve the codebase slightly.

**The Cost of Messy Code**: Teams that start fast with messy code slow to a crawl within months. Productivity approaches zero as the mess grows. The only way to go fast is to keep the code clean.

### Chapter 2: Meaningful Names

**Use Intention-Revealing Names**
```
Bad:  int d; // elapsed time in days
Good: int elapsedTimeInDays;
Good: int daysSinceCreation;
Good: int daysSinceModification;
Good: int fileAgeInDays;
```

**Avoid Disinformation**
- Don't use `accountList` unless it's actually a List (use `accounts` or `accountGroup`)
- Avoid names that vary in small ways: `XYZControllerForEfficientHandlingOfStrings` vs `XYZControllerForEfficientStorageOfStrings`
- Avoid using lowercase `L` or uppercase `O` as variable names (look like 1 and 0)

**Make Meaningful Distinctions**
- Number-series naming (`a1`, `a2`, `aN`) is the opposite of intentional naming
- Noise words are meaningless distinctions: `ProductInfo` vs `ProductData`, `CustomerObject` vs `Customer`
- `getActiveAccount()` vs `getActiveAccountInfo()` — how do callers know which to use?

**Use Pronounceable Names**
```
Bad:  genymdhms (generation date, year, month, day, hour, minute, second)
Good: generationTimestamp
```

**Use Searchable Names**
- Single-letter names and numeric constants are hard to locate
- The length of a name should correspond to the size of its scope
- `MAX_CLASSES_PER_STUDENT` is better than `7`

**Avoid Encodings**
- Hungarian notation is obsolete with modern IDEs
- Don't prefix member variables (`m_`, `_`)
- Don't prefix interfaces with `I` — prefer `ShapeFactory` over `IShapeFactory`

**Class Names**: Should be nouns or noun phrases: `Customer`, `WikiPage`, `Account`, `AddressParser`. Never verbs. Avoid `Manager`, `Processor`, `Data`, `Info`.

**Method Names**: Should be verbs or verb phrases: `postPayment`, `deletePage`, `save`. Accessors/mutators/predicates: `get`, `set`, `is` prefix.

**Pick One Word Per Concept**: Don't use `fetch`, `retrieve`, and `get` for equivalent methods in different classes. Be consistent.

**Don't Pun**: Avoid using the same word for two different purposes. If `add` creates a new value by adding two values, don't use `add` for putting an element in a collection — use `insert` or `append`.

**Use Solution Domain Names**: `AccountVisitor`, `JobQueue` — programmers will know these patterns.

**Use Problem Domain Names**: When no solution domain term exists, use terms from the problem domain.

**Add Meaningful Context**: `firstName`, `lastName`, `street`, `city`, `state` — without context, `state` is ambiguous. Better: `addrFirstName`, `addrState` or wrap in an `Address` class.

**Don't Add Gratuitous Context**: In an app named "Gas Station Deluxe", don't prefix every class with `GSD`. `GSDAccountAddress` is worse than `AccountAddress`.

### Chapter 3: Functions

**Small!**
- Functions should be small. Then smaller than that.
- 20 lines maximum, ideally under 10
- Blocks within `if`, `else`, `while` should be one line long — probably a function call
- Indent level should not exceed one or two

**Do One Thing**
- Functions should do one thing, do it well, and do it only
- Test: Can you extract another function from it with a name that's not a restatement of the implementation?
- A function that handles only steps one level of abstraction below its name is doing one thing

**One Level of Abstraction Per Function**
- Don't mix high-level concepts with low-level details
- Reading code should be like reading a top-down narrative: "To do X, we do A, then B, then C. To do A, we..."
- The Stepdown Rule: Every function should be followed by functions at the next level of abstraction

**Switch Statements**
- Inherently violate "do one thing"
- Bury them in low-level classes using polymorphism
- Use Abstract Factory to hide them

**Use Descriptive Names**
- `includeSetupAndTeardownPages` is better than `testableHtml`
- Long descriptive names are better than short enigmatic names
- Long descriptive names are better than long descriptive comments
- Be consistent in naming conventions

**Function Arguments**
- Ideal: zero (niladic)
- Good: one (monadic)
- Acceptable: two (dyadic)
- Questionable: three (triadic)
- Bad: more than three (polyadic) — requires strong justification

**Common Monadic Forms**
- Asking a question: `boolean fileExists("MyFile")`
- Transforming: `InputStream fileOpen("MyFile")`
- Event: `void passwordAttemptFailedNtimes(int attempts)`

**Flag Arguments**: Ugly. Passing a boolean says the function does more than one thing. Split into two functions.

**Dyadic Functions**: `writeField(name)` is better than `writeField(outputStream, name)`. Make `outputStream` a member variable.

**Argument Objects**: When functions need 2-3+ arguments, some likely warrant wrapping:
```
Circle makeCircle(double x, double y, double radius);
Circle makeCircle(Point center, double radius);
```

**Verbs and Keywords**: Monad should be verb/noun pair: `write(name)`, `writeField(name)`. Keyword form encodes arguments: `assertExpectedEqualsActual(expected, actual)`.

**Have No Side Effects**
- Side effects are lies — function promises one thing, does hidden things too
- Creates temporal coupling and order dependencies
- `checkPassword()` that also initializes a session couples password checking to session initialization

**Command Query Separation**
- Functions should either DO something OR answer something, not both
- `if (set("username", "unclebob"))...` — is this asking if "username" was previously "unclebob" or if it was set successfully?
- Better: `if (attributeExists("username")) { setAttribute("username", "unclebob"); }`

**Prefer Exceptions to Error Codes**
- Error codes cause deeply nested structures
- Extract try/catch blocks into functions: `try { deletePage(page); } catch (Exception e) { logError(e); }`
- Error handling IS one thing — function that handles errors should do nothing else
- `Error.java` dependency magnet — adding new errors requires recompilation

**Don't Repeat Yourself (DRY)**
- Duplication is the root of all evil in software
- Every duplication represents missed abstraction opportunity
- Object-oriented, structured, aspect-oriented programming all aim to eliminate duplication

**Structured Programming**
- Dijkstra's rule: one entry, one exit per function
- Only important for large functions
- Small functions: multiple returns, break, continue are fine

**How to Write Functions Like This**
- First draft is clumsy, long, nested, arbitrary names, duplicate code
- Then massage and refine: break out functions, rename, eliminate duplication
- Shrink and rearrange while keeping tests passing

### Chapter 4: Comments

**Comments Don't Make Up for Bad Code**
- Clear code with few comments > cluttered code with lots of comments
- Don't comment bad code — rewrite it

**Explain Yourself in Code**
```
Bad:  // Check if employee is eligible for benefits
      if ((employee.flags & HOURLY_FLAG) && (employee.age > 65))
Good: if (employee.isEligibleForFullBenefits())
```

**Good Comments**

*Legal Comments*: Copyright, authorship statements required by corporate standards

*Informative Comments*: `// format matched kk:mm:ss EEE, MMM dd, yyyy` — though a class named `DateTimeFormatter` is better

*Explanation of Intent*: Why, not what — `// This is our best attempt to get a race condition...`

*Clarification*: When using standard library or code you can't alter: `assertTrue(a.compareTo(b) == -1); // a < b`

*Warning of Consequences*: `// Don't run unless you have time to kill`

*TODO Comments*: Jobs that should be done but can't be done right now. Not an excuse to leave bad code.

*Amplification*: Emphasizes importance of something that may seem inconsequential

*Javadocs in Public APIs*: If writing a public API, write good Javadocs

**Bad Comments**

*Mumbling*: Comments because you feel you should or process requires it

*Redundant Comments*: Takes longer to read than the code
```java
// The processor delay for this component
protected int backgroundProcessorDelay = -1;
```

*Misleading Comments*: Stating something slightly incorrect

*Mandated Comments*: Javadocs for every function — clutters code, propagates lies

*Journal Comments*: Log of changes — that's what source control is for

*Noise Comments*: `/** The name. */ private String name;`

*Scary Noise*: Copy-paste Javadocs with wrong information

*Don't Use Comments When You Can Use a Function or Variable*
```
Bad:  // does the module from the global list depend on subsystem?
      if (smodule.getDependSubsystems().contains(subSysMod.getSubSystem()))
Good: ArrayList moduleDependees = smodule.getDependSubsystems();
      String ourSubSystem = subSysMod.getSubSystem();
      if (moduleDependees.contains(ourSubSystem))
```

*Position Markers*: `// Actions /////////////////////` — noise, ignore them

*Closing Brace Comments*: `} // while` — indicates function is too long

*Attributions and Bylines*: Source control handles this

*Commented-Out Code*: Delete it. Source control remembers.

*HTML Comments*: Hard to read, tools should add HTML

*Nonlocal Information*: Don't describe system-wide things in local comment

*Too Much Information*: Don't put historical discussions in comments

*Inobvious Connection*: Comment and code must be obviously connected

*Function Headers*: Short functions with good names don't need headers

*Javadocs in Nonpublic Code*: Formality is distraction in internal code

### Chapter 5: Formatting

**Purpose of Formatting**: Communication. Code changes, but style and discipline survive.

**Vertical Formatting**
- Significant projects (FitNesse, JUnit) average 200 lines per file, max around 500
- Smaller files are easier to understand

**The Newspaper Metaphor**
- Name should tell if you're in the right module
- Top should give high-level concepts
- Detail increases as you move down
- Newspaper: headline, synopsis, details, dates, names

**Vertical Openness Between Concepts**: Blank lines separate distinct concepts

**Vertical Density**: Lines that are tightly related should appear close together

**Vertical Distance**
- Closely related concepts should be vertically close
- Variable declarations: as close to usage as possible
- Instance variables: at the top of the class (Java) or bottom (C++)
- Dependent functions: caller above callee, close together
- Conceptual affinity: similar functions grouped together

**Vertical Ordering**: Caller above callee creates nice top-down flow

**Horizontal Formatting**
- Lines should be 80-120 characters max
- Never scroll right

**Horizontal Openness and Density**
- Spaces around assignment: `int lineSize = line.length();`
- No space between function and parens: `lineWidthHistogram.addLine(lineSize)`
- Spaces around operators based on precedence: `b*b - 4*a*c`

**Horizontal Alignment**: Don't align variable names or values in columns — draws eye away from actual info

**Indentation**: File → class → method → block → block. Each level is a scope.

**Breaking Indentation**: Don't collapse short `if` statements to one line

**Team Rules**: Every team member should format the same way. Agree on style guide.

### Chapter 6: Objects and Data Structures

**Data Abstraction**
- Don't blindly add getters/setters — that exposes implementation
- Abstract interface lets you manipulate essence without knowing implementation
- `getFuelTankCapacityInGallons()` vs `getPercentFuelRemaining()` — latter hides vehicle type

**Data/Object Anti-Symmetry**
- Objects hide data, expose behavior
- Data structures expose data, have no behavior
- They are virtual opposites

**Procedural Code**: Easy to add new functions (don't change data structures), hard to add new data structures (change all functions)

**OO Code**: Easy to add new classes (don't change functions), hard to add new functions (change all classes)

**The Law of Demeter**: Module shouldn't know innards of objects it manipulates
- Method `f` of class `C` should only call methods of: `C`, objects created by `f`, objects passed to `f`, objects held in instance variables of `C`
- Don't call methods on objects returned by allowed methods

**Train Wrecks**: `a.getB().getC().doSomething()` — violates Demeter. But OK if a, B, C are data structures.

**Hybrids**: Half object, half data structure — worst of both worlds. Avoid.

**Data Transfer Objects (DTOs)**
- Pure data structures: public variables, no functions
- Useful for database communication, parsing messages
- Beans (private variables with getters/setters) offer no real benefit

**Active Record**
- DTOs with navigational methods (save, find)
- Don't add business methods — that creates hybrid
- Treat as data structure, put business rules in separate objects

### Chapter 7: Error Handling

**Use Exceptions Rather Than Return Codes**
- Return codes clutter caller with error checking
- Exceptions separate error handling from happy path

**Write Try-Catch-Finally First**
- Exceptions define scope within program
- Try block is like a transaction — catch leaves program in consistent state
- TDD: Write test that expects exception, then write code

**Use Unchecked Exceptions**
- Checked exceptions violate Open/Closed Principle
- Low-level change forces signature changes through many layers
- Cost of checked exceptions outweighs benefits for general applications

**Provide Context with Exceptions**
- Create informative error messages
- Include failed operation and failure type
- Logging: include enough to diagnose where failure occurred

**Define Exception Classes by Caller's Needs**
- Classify by how they're caught
- Often a single exception type per component is enough
- Wrap third-party APIs to throw your own exception types

**Define the Normal Flow**
```java
// Exception clutters business logic
try {
    MealExpenses expenses = expenseReportDAO.getMeals(employee.getID());
    total += expenses.getTotal();
} catch(MealExpensesNotFound e) {
    total += getMealPerDiem();
}

// Special Case Pattern - cleaner
MealExpenses expenses = expenseReportDAO.getMeals(employee.getID());
total += expenses.getTotal();
// DAO returns PerDiemMealExpenses if no meals found
```

**Don't Return Null**
- Returning null creates work for caller and risk of NullPointerException
- Throw exception or return Special Case object instead
- If tempted to return null from third-party method, wrap it

**Don't Pass Null**
- Returning null is bad, passing null is worse
- No good way to handle null passed by caller
- Most languages don't help with accidentally passed nulls

### Chapter 8: Boundaries

**Using Third-Party Code**
- Providers want broad applicability; users want focused interface
- `Map<String, Sensor>` exposes too much — wrap it: `Sensors.getById(String id)`
- Don't pass Maps (or any boundary interface) around your system

**Exploring and Learning Boundaries**
- Write learning tests to understand third-party code
- Controlled experiments that test our understanding
- When new versions release, learning tests verify behavior still matches

**Learning log4j**: Example of writing tests to understand API before using it

**Learning Tests Are Better Than Free**
- Cost nothing (we have to learn API anyway)
- Investment that pays back when third-party releases new version
- Verify third-party packages work as expected

**Using Code That Doesn't Yet Exist**
- Create interface for what you wish third-party provided
- Adapter pattern connects your interface to third-party when ready
- Keeps your code clean while third-party is unknown

**Clean Boundaries**
- Minimize what knows about third-party particulars
- Depend on what YOU control
- Wrap or use Adapter to convert third-party interface to yours
- Code is more readable, boundary easier to migrate when third-party changes

### Chapter 9: Unit Tests

**The Three Laws of TDD**
1. Don't write production code until you have failing unit test
2. Don't write more of unit test than sufficient to fail
3. Don't write more production code than sufficient to pass the test

**Keeping Tests Clean**
- Test code is just as important as production code
- Dirty tests are worse than no tests — impossible to maintain
- Tests enable change — without them, every change is a possible bug

**Clean Tests: Readability**
- Clarity, simplicity, density of expression
- Build-Operate-Check pattern: build test data, operate on it, check results
- Domain-specific testing language: custom functions and utilities for tests

**One Assert Per Test**
- Makes tests easy to understand
- Single concept per test is the real rule
- Multiple asserts OK if testing one concept

**F.I.R.S.T.**
- **Fast**: Tests should run quickly
- **Independent**: Tests shouldn't depend on each other
- **Repeatable**: Run in any environment (prod, QA, laptop, train)
- **Self-Validating**: Boolean output — pass or fail
- **Timely**: Written just before production code

### Chapter 10: Classes

**Class Organization**
- Public static constants first
- Private static variables
- Private instance variables
- Public functions
- Private utilities called by public functions right after

**Encapsulation**: Keep variables and utility functions private. Loosen only for tests, reluctantly.

**Classes Should Be Small!**
- Measured by responsibilities, not lines of code
- Name describes responsibilities — avoid words like "Processor", "Manager", "Super"
- 25-word description without "if", "and", "or", "but"

**Single Responsibility Principle (SRP)**
- Class should have one and only one reason to change
- Getting software to work and making it clean are different activities
- Many small classes > few large classes

**Cohesion**
- Small number of instance variables
- Each method should manipulate one or more of those variables
- More variables a method manipulates = more cohesive to its class
- When cohesion is high, methods and variables co-depend, hang together as a whole

**Maintaining Cohesion Results in Many Small Classes**
- Breaking large functions creates classes
- When function variable becomes instance variable, other functions can use it
- When some functions share variables, they should become their own class

**Organizing for Change**
- Classes should be open for extension, closed for modification
- New features should extend, not modify
- Isolate from change with abstractions

**Dependency Inversion Principle (DIP)**
- Classes should depend on abstractions, not concrete details
- Makes testing easier (inject mock implementations)
- System is more flexible, reusable

### Chapter 11: Systems

**Separate Constructing from Using**
- Software systems should separate startup (object construction) from runtime logic
- Construction is a very different process from use
- Mixing the two makes testing harder

**Separation of Main**
- Main builds objects needed by system, passes to application
- Application has no knowledge of main or construction
- All arrows point from main toward application

**Factories**: When application needs to control when objects are created, use Abstract Factory

**Dependency Injection**
- Object shouldn't instantiate dependencies itself
- Separate construction into separate "main" module
- Container controls injection of dependencies

**Scaling Up**
- Can't get systems right the first time
- Implement today's stories, refactor and expand tomorrow
- Iterative and incremental agility

**Cross-Cutting Concerns**
- Some concerns (logging, security, transactions) cross object boundaries
- Aspect-Oriented Programming (AOP) addresses this
- Modularize cross-cutting concerns

**Test Drive the System Architecture**
- Big Design Up Front (BDUF) is harmful
- Optimal architecture consists of modularized domains of concern
- Different domains can use different technologies

**Optimize Decision Making**
- Modularity and separation of concerns make decentralized management possible
- Give responsibilities to most qualified persons
- Postpone decisions until the last responsible moment (most information available)

**Use Standards Wisely**: Standards make it easier to reuse ideas and components, but can be over-engineered

**Systems Need Domain-Specific Languages (DSLs)**
- Good DSLs minimize communication gap between domain concept and code
- DSLs raise level of abstraction above code idioms and design patterns

### Chapter 12: Emergence

**Kent Beck's Four Rules of Simple Design** (in order of importance):
1. Runs all the tests
2. Contains no duplication
3. Expresses programmer's intent
4. Minimizes number of classes and methods

**Running All the Tests**
- System must be testable to be verified
- Making testable systems pushes toward small, single-purpose classes
- Tight coupling makes tests hard to write
- More tests = more we push toward testable design = better design

**Refactoring**
- Once tests exist, we can refactor without fear
- Incrementally clean up during refactoring
- Apply all knowledge: cohesion, decoupling, separation of concerns

**No Duplication**
- Duplication is primary enemy of well-designed systems
- Duplication = additional work, risk, complexity
- Template Method pattern removes higher-level duplication

**Expressive**
- Code should clearly express author's intent
- Good names
- Small functions and classes
- Standard nomenclature (design pattern names)
- Well-written unit tests as documentation
- Care: take pride in your workmanship

**Minimal Classes and Methods**
- Keep count low, but this rule is lowest priority
- Don't create classes just for the sake of it
- Pragmatism over dogmatism

### Chapter 13: Concurrency

**Why Concurrency?**
- Decoupling strategy: separate what from when
- Can improve throughput and structure
- Example: many users, each gets their own thread

**Myths and Misconceptions**
- Concurrency does NOT always improve performance
- Design DOES change when writing concurrent code
- Understanding concurrency issues IS important (even with containers)

**Challenges**
- Many possible execution paths
- Some paths produce incorrect results
- Failures are often hard to reproduce

**Concurrency Defense Principles**

*Single Responsibility Principle*: Separate concurrency code from other code

*Corollary: Limit Scope of Data*: Use `synchronized` to protect critical sections. Minimize shared data.

*Corollary: Use Copies of Data*: Avoid sharing by copying data

*Corollary: Threads Should Be as Independent as Possible*: Each thread processes one request, no shared state

**Know Your Library**
- Thread-safe collections
- Executor framework
- Non-blocking solutions
- Library classes not thread-safe

**Know Your Execution Models**
- Producer-Consumer
- Readers-Writers
- Dining Philosophers

**Beware Dependencies Between Synchronized Methods**: Avoid using more than one method on shared object

**Keep Synchronized Sections Small**: Locks are expensive, minimize critical sections

**Writing Correct Shut-Down Code Is Hard**: Think about shut-down early, get it working early

**Testing Threaded Code**
- Write tests that expose problems, run frequently with different configurations
- Treat spurious failures as potential threading issues
- Get non-threaded code working first
- Make threaded code pluggable and tunable
- Run with more threads than processors
- Run on different platforms
- Instrument code to force different orderings

### Chapter 14-16: Successive Refinement, JUnit Internals, Refactoring SerialDate

**Key Lessons**
- Code is never "done" — it can always be improved
- Refactoring is continuous, incremental process
- Leave code cleaner than you found it
- Every change should make the code better
- Craftsmanship requires constant attention and care

### Chapter 17: Smells and Heuristics

**Comments**
- C1: Inappropriate Information — belongs in source control, issue tracker
- C2: Obsolete Comment — comment that has gotten old
- C3: Redundant Comment — describes something that adequately describes itself
- C4: Poorly Written Comment — grammar, punctuation, be brief
- C5: Commented-Out Code — delete it

**Environment**
- E1: Build Requires More Than One Step
- E2: Tests Require More Than One Step

**Functions**
- F1: Too Many Arguments
- F2: Output Arguments — readers expect arguments as inputs
- F3: Flag Arguments — functions that do more than one thing
- F4: Dead Function — never called, delete it

**General**
- G1: Multiple Languages in One Source File
- G2: Obvious Behavior Is Unimplemented — surprises and breaks trust
- G3: Incorrect Behavior at Boundaries — don't rely on intuition, test boundaries
- G4: Overridden Safeties — don't turn off failing tests, compiler warnings
- G5: Duplication — DRY, most important rule
- G6: Code at Wrong Level of Abstraction
- G7: Base Classes Depending on Derivatives
- G8: Too Much Information — well-defined interfaces have few methods, low coupling
- G9: Dead Code — code that isn't executed, delete it
- G10: Vertical Separation — variables and functions should be close to usage
- G11: Inconsistency — if you do something a certain way, do all similar things that way
- G12: Clutter — unused variables, uncalled functions, delete them
- G13: Artificial Coupling — things that don't depend on each other shouldn't be coupled
- G14: Feature Envy — methods that use other class's accessors
- G15: Selector Arguments — function that selects behavior based on argument
- G16: Obscured Intent — code should be as expressive as possible
- G17: Misplaced Responsibility — code should be where reader expects it
- G18: Inappropriate Static — prefer non-static methods when in doubt
- G19: Use Explanatory Variables — break up calculations with intermediate variables
- G20: Function Names Should Say What They Do
- G21: Understand the Algorithm — understand why it works, not just that it works
- G22: Make Logical Dependencies Physical
- G23: Prefer Polymorphism to If/Else or Switch/Case
- G24: Follow Standard Conventions
- G25: Replace Magic Numbers with Named Constants
- G26: Be Precise — don't be lazy about decisions
- G27: Structure Over Convention — enforce design decisions with structure
- G28: Encapsulate Conditionals — `if (shouldBeDeleted(timer))` > `if (timer.hasExpired() && !timer.isRecurrent())`
- G29: Avoid Negative Conditionals — `if (buffer.shouldCompact())` > `if (!buffer.shouldNotCompact())`
- G30: Functions Should Do One Thing
- G31: Hidden Temporal Couplings — make temporal coupling explicit
- G32: Don't Be Arbitrary — have a reason for structure
- G33: Encapsulate Boundary Conditions — `nextLevel = level + 1` instead of using `level + 1` everywhere
- G34: Functions Should Descend Only One Level of Abstraction
- G35: Keep Configurable Data at High Levels
- G36: Avoid Transitive Navigation — Law of Demeter

**Java**
- J1: Avoid Long Import Lists by Using Wildcards
- J2: Don't Inherit Constants — use static import
- J3: Constants versus Enums — use enums

**Names**
- N1: Choose Descriptive Names
- N2: Choose Names at Appropriate Level of Abstraction
- N3: Use Standard Nomenclature Where Possible — pattern names, ubiquitous language
- N4: Unambiguous Names
- N5: Use Long Names for Long Scopes — short names OK for short scopes
- N6: Avoid Encodings — no Hungarian, no prefixes
- N7: Names Should Describe Side Effects

**Tests**
- T1: Insufficient Tests — test everything that could break
- T2: Use a Coverage Tool
- T3: Don't Skip Trivial Tests
- T4: An Ignored Test Is a Question About an Ambiguity
- T5: Test Boundary Conditions
- T6: Exhaustively Test Near Bugs — bugs cluster
- T7: Patterns of Failure Are Revealing
- T8: Test Coverage Patterns Can Be Revealing
- T9: Tests Should Be Fast

---

## THE PRAGMATIC PROGRAMMER (Thomas & Hunt)

### Chapter 1: A Pragmatic Philosophy

**It's Your Life**
- You have agency over your career and work
- "I can't do X because Y" — is it really impossible?
- If your job is frustrating, fix it or find a new one
- Invest in yourself, don't wait for company training

**The Cat Ate My Source Code**
- Take responsibility for yourself and your actions
- Don't blame others or make excuses
- When something goes wrong, provide options, not excuses
- "What can I do to fix this?" not "It's not my fault"

**Software Entropy**
- Broken Window Theory: One broken window leads to decay
- Don't leave bad code unfixed — fix it now or board it up (TODO + ticket)
- Don't cause collateral damage just because there's existing mess
- Be the catalyst for positive change

**Stone Soup and Boiled Frogs**
- Stone Soup: Be a catalyst — show them a glimpse of future, get them to rally
- Boiled Frog: Watch for gradual changes that sneak up on you
- Keep an eye on the big picture — are you in boiling water?

**Good-Enough Software**
- Know when to stop: perfect is the enemy of good
- Give users something to criticize early
- Great software today > perfect software never
- But "good enough" doesn't mean sloppy or incomplete

**Your Knowledge Portfolio**
- Your knowledge is your most important professional asset
- It expires like investments — must continually reinvest
- Manage like financial portfolio: diversify, balance risk, buy low sell high, rebalance

**Portfolio Building**
- Learn one new language per year
- Read one technical book per month
- Read non-technical books too
- Take classes
- Participate in local user groups and meetups
- Experiment with different environments
- Stay current: read blogs, HN, papers

**Communicate!**
- Know your audience — what do they need to know?
- Know what you want to say — plan it
- Choose the right moment — timing matters
- Choose a style — adjust formality to audience
- Make it look good — presentation matters
- Involve your audience — ask questions
- Be a listener — encourage questions
- Get back to people — follow up

### Chapter 2: A Pragmatic Approach

**The Essence of Good Design**
- ETC: Easy To Change
- Why is decoupling good? Because it's ETC
- Why is single responsibility good? Because it's ETC
- Every design decision: "Did I make the code easier to change?"

**DRY — Don't Repeat Yourself**
- Every piece of knowledge must have single, unambiguous representation
- Not just code duplication — knowledge duplication
- Types of duplication:
  - **Imposed**: Developer sees no choice (but there usually is)
  - **Inadvertent**: Didn't realize it was duplication
  - **Impatient**: Lazy shortcut "I'll clean it up later"
  - **Interdeveloper**: Multiple devs duplicate information

**DRY in Code**: Extract functions, use code generation

**DRY in Documentation**: Don't repeat code in comments — code should be self-documenting. Generate docs from code.

**DRY in Data**: Database schemas and code structs — generate one from the other. Normalize data.

**DRY Between Developers**: Communication is key. Good codebase structure helps. Active developers know who is working on what.

**Orthogonality**
- Two things are orthogonal if changes in one don't affect the other
- Nonorthogonal systems are harder to change — change in one area ripples
- Benefits: increased productivity, reduced risk, easier testing

**Designing Orthogonal Systems**
- Design independent, self-contained components
- Ask: "If I change X, how many things break?"
- Don't rely on things you can't control
- Layer your system

**Coding Orthogonality**
- Keep code decoupled
- Avoid global data
- Avoid similar functions — they share common algorithm? Factor it out.
- Get into habit of being constantly critical of code

**Testing Orthogonality**
- Orthogonal systems easier to test
- Unit tests are inherently orthogonal
- Bug fix in one area shouldn't affect others

**Reversibility**
- Critical decisions are hard to reverse
- Make them reversible: flexibility is key
- There are no final decisions — requirements, vendors, platforms change
- Don't commit to particulars until you have to

**Flexible Architecture**
- Abstract away things that might change
- Hide third-party APIs behind your own interfaces
- Break code into components

**Tracer Bullets**
- When you're not sure how to hit the target, use tracer bullets
- Get something working end-to-end immediately
- Build a skeleton of final application
- Tracer code is lean but complete: users see something working early, developers have a structure to build on

**Tracer Bullets vs Prototypes**
- Tracer bullets are kept and built upon
- Prototypes are thrown away
- Tracer bullets might miss — that's OK, adjust and fire again

**Prototypes and Post-it Notes**
- Prototype to learn — code that gets thrown away
- What to prototype: risky or uncertain things
- Prototyping lets you try things that would be too risky in production
- When done, throw it away and do it right

**What to Prototype**
- Architecture
- New functionality
- Structure of external data
- Third-party tools
- Performance issues
- User interface design

**How to Prototype**
- Ignore correctness, completeness, robustness, style
- Use high-level languages or tools
- Focus on specific aspects being examined

**Domain Languages**
- Program close to the problem domain
- Consider creating mini-languages for common tasks
- Internal DSLs (within host language) vs External DSLs (separate parser)
- Trade-off: power vs complexity of implementation

**Estimating**
- Estimates come from understanding
- Build a model of the system
- Break model into components
- Identify parameters
- Calculate answers

**How Accurate Is Accurate Enough?**
- Units matter: "about 6 months" vs "130 working days"
- 1-15 days → days; 3-6 weeks → weeks; 8-20 weeks → months; 20+ weeks → think carefully
- Avoid false precision

**Where Do Estimates Come From?**
- Ask someone who's done it
- Understand what's being asked
- Build a mental model
- Break into components
- Give each parameter a value
- Calculate
- Track actual values to improve

**Estimating Project Schedules**
- Initial estimates are guesses
- Iterative schedules: implement incrementally
- After each iteration, refine schedule based on actuals
- The schedule gets more accurate as project progresses

**What to Say When Asked for an Estimate**: "I'll get back to you"

### Chapter 3: The Basic Tools

**The Power of Plain Text**
- Human-readable data outlasts applications that created it
- Plain text won't be obsolete
- Self-describing, easier to test, easier to process

**Shell Games**
- Get fluent with shell
- Customize your shell
- Aliases, functions, scripts
- GUI is limited; shell is powerful

**Power Editing**
- Achieve editor fluency — learn one editor well
- When you learn a new trick, use it
- Grow your editor with extensions

**Editor Features to Master**
- Selecting/cutting/pasting text
- Moving by characters, words, lines, blocks
- Moving by syntactic units
- Re-indenting code
- Code completion
- Multi-cursor editing
- Window splitting
- Navigation to definition
- Refactoring commands

**Version Control**
- Always use version control
- For everything: code, docs, config, scripts, notes
- Branch for experiments
- Commit often with meaningful messages

**Debugging**
- Fix the problem, not the blame
- Don't panic — think rationally
- Reproduce the bug first
- Read error messages — really read them
- Failing test case = bug captured forever

**Debugging Strategies**
- Binary search — isolate the problem
- Rubber ducking — explain to someone (or something)
- Process of elimination — prove your assumptions
- If something "can't happen," check for bad data
- Tracing — watch the program flow
- The bug is probably in your code (not the compiler, OS, or library)

**Text Manipulation**
- Learn a text manipulation language (sed, awk, Python, Perl)
- Useful for: build automation, code generation, testing

**Engineering Daybooks**
- Keep a journal of what you do
- Helps you remember, lets you reflect
- Paper or digital — whatever works

### Chapter 4: Pragmatic Paranoia

**Design by Contract**
- Document and verify module expectations
- Preconditions: what must be true before calling
- Postconditions: what is guaranteed after
- Class invariants: what is always true

**DBC vs Defensive Programming**
- DBC: verify preconditions, guarantee postconditions, crash if violated
- Defensive: check everything, try to continue
- DBC makes errors obvious; defensive programming can hide them

**Dead Programs Tell No Lies**
- All errors give information
- Crashes are better than silently corrupting data
- Don't ignore errors — if something "can't happen," crash if it does

**Crash, Don't Trash**
- Crash early: stop before corrupting data
- Better to fail than to spread corruption
- Supervisors can restart clean

**Assertive Programming**
- Use assertions to check things that can't happen
- Don't use assertions for things that can fail in production
- Leave assertions on in production (usually)
- Assert with a message

**How to Balance Resources**
- Finish what you start: allocate → use → deallocate
- Allocator should deallocate
- Nest allocations in opposite order
- Allocate all resources together or transaction-style

**Resource Balancing Strategies**
- Objects: allocate in constructor, deallocate in finalizer/dispose
- Finally blocks, using statements
- Resource wrappers

**Don't Outrun Your Headlights**
- Take small steps
- Get feedback frequently
- Don't predict too far into the future
- Design for what you know NOW

### Chapter 5: Bend, or Break

**Decoupling**
- Coupling ties things together — change ripples through coupled systems
- Train wrecks: `a.getB().getC().doSomething()` — each dot is a coupling
- Shy code: don't reveal yourself, don't interact with too many things

**Tell, Don't Ask**
- Don't ask object for state, make decision, tell it what to do
- Just tell object what you need done
- Let object figure out how

**The Law of Demeter**
- Method should only call methods of: its class, objects it creates, parameters, direct components
- Reduces coupling — object only talks to friends

**Configuring**
- Parameterize app with external configuration
- Keep specifics out of code
- Configuration-as-a-Service for dynamic config

**Juggling the Real World**
- Events: things happen, code reacts
- Finite State Machines for event-driven state transitions
- Observer Pattern: decouple event sources from handlers
- Publish/Subscribe: channels between publishers and subscribers
- Reactive Programming: streams of events

**Transforming Programming**
- Think of programs as transformations: input → output
- Programming is about data transformation
- Pipelines: chain transformations
- Embrace functional thinking even in OO languages

**Inheritance Tax**
- Inheritance creates coupling
- Prefer interfaces to inheritance
- Prefer delegation to inheritance
- Prefer mixins to inheritance

**Alternatives to Inheritance**
- Interfaces/protocols: polymorphism without hierarchy
- Delegation: has-a vs is-a
- Mixins/traits: share implementation without inheritance

### Chapter 6: Concurrency

**Breaking Temporal Coupling**
- Find what can happen at same time
- Activity diagrams to analyze workflow
- Maximize parallelism in design

**Parallelism**
- Multiple tasks at once on multi-core/distributed
- Independent subprocesses
- Communication via queues or shared memory

**Shared State Is Incorrect State**
- If two processes access same memory, you have potential race condition
- Semaphores/mutexes protect shared resources
- Better: avoid shared state entirely

**Actors and Processes**
- Actor: independent process with mailbox
- No shared state between actors
- Communicate only via messages
- Supervision: actors watch other actors

### Chapter 7: While You Are Coding

**Listen to Your Lizard Brain**
- If something feels wrong, pay attention
- Instincts are pattern recognition from experience
- Trust your gut, but verify rationally

**Programming by Coincidence**
- Don't program by coincidence
- Know WHY your code works
- Don't rely on accidents — they'll break
- Code deliberately, test assumptions

**How to Program Deliberately**
- Always be aware of what you're doing
- Can you explain the code to a junior?
- Don't code blindfolded
- Have a plan
- Rely only on documented behavior
- Document your assumptions
- Test assumptions, not just code
- Don't let existing code dictate future code
- Refactor early and often

**Algorithm Speed**
- Know Big-O notation
- Understand complexity of algorithms you use
- Test your estimates with real data
- Best isn't always best — context matters

**Common Big-O**
- O(1): constant — hash lookup
- O(log n): logarithmic — binary search
- O(n): linear — sequential search
- O(n log n): linearithmic — quicksort, mergesort
- O(n²): quadratic — nested loops
- O(2^n): exponential — traveling salesman

**Refactoring**
- Refactor early, refactor often
- Don't refactor and add functionality simultaneously
- Have good tests first
- Take short, deliberate steps
- Test after each step

**When to Refactor**
- Duplication (DRY violation)
- Non-orthogonal design
- Outdated knowledge
- Usage patterns changed
- Performance
- The tests pass (good time to clean up!)

**Testing to Code**
- Test-first thinking improves design
- Test-driven design: test → code → refactor
- Testing IS design: tests explore module's API
- Focus on tests, not testing (verb vs noun)

**Property-Based Testing**
- Test contracts/invariants, not specific values
- Generate many random inputs
- Find edge cases you wouldn't think of

**Stay Safe Out There**
- Security is a habit, not a feature
- Minimize attack surface
- Principle of least privilege
- Secure defaults
- Encrypt sensitive data
- Don't trust input

**Naming Things**
- Names should express intent
- Communicate meaning
- Rename when meaning changes
- Consistent naming within project

### Chapter 8: Before the Project

**The Requirements Pit**
- Requirements rarely exist — they have to be dug out
- Don't gather requirements — discover them
- Work with users to understand their actual needs
- Requirements are learned in feedback loops

**Requirements Are a Process**
- Requirements change, and that's OK
- Short iterations give feedback
- Build a little, show a little, learn a little
- Walk in user's shoes

**Solving Impossible Puzzles**
- Real constraints vs imagined constraints
- Ask: What is actually stopping you?
- Some constraints are illusions
- Think outside the box — or identify the actual box

**Working Together**
- Pair programming, mob programming
- Real-time code reviews
- Build systems, don't point fingers
- You + team > sum of individuals

**The Essence of Agility**
- Agility is a response to change
- Values: individuals and interactions, working software, collaboration, responding to change
- Do what works for you
- Context matters more than rules

### Chapter 9: Pragmatic Projects

**Pragmatic Teams**
- No broken windows — team quality
- Boiled frogs — team awareness
- Schedule time for improvement
- Communicate internally and externally
- DRY between team members
- Orthogonal teams: clear responsibilities

**Automation**
- Automate everything
- Build, test, deploy
- Don't rely on manual steps
- Continuous integration
- Consistency > heroics

**Ruthless Testing**
- Find bugs before users do
- Test early, test often, test automatically
- Test the tests: does the test catch bugs?
- Test state coverage, not code coverage

**Types of Tests**
- Unit: single module
- Integration: modules together
- Validation: users' requirements
- Resource exhaustion: memory, disk, network
- Performance: speed, load
- Usability: real users

**When to Test**
- After every edit (automated)
- Before commit (automated)
- Before release (extensive)
- After bugs are found (test to prevent recurrence)

**Naming Conventions**
- Use project naming conventions
- Communicate through code
- Names document purpose

**Write Code That Writes Code**
- Code generators: passive (run once) vs active (run always)
- DSLs, template engines
- Reduce boring, error-prone tasks

**Delight Your Users**
- We're building solutions, not writing code
- Users don't care about technology
- Solve the actual problem
- Make users successful

**Pride and Prejudice**
- Sign your work
- Take pride in your craft
- Build things you're proud to put your name on
- Professional responsibility

---

## DESIGNING DATA-INTENSIVE APPLICATIONS (Martin Kleppmann)

### Part I: Foundations of Data Systems

**Chapter 1: Reliable, Scalable, and Maintainable Applications**

**Reliability**
- System continues to work correctly even when things go wrong
- Fault: component deviating from spec
- Failure: system as a whole stops providing required service
- Build fault-tolerant systems: prevent faults from causing failures

**Types of Faults**
- Hardware faults: disk crash, RAM errors, power grid blackout
- Software errors: systematic bugs, runaway processes, cascading failures
- Human errors: configuration mistakes, deploying bad code

**Mitigating Human Errors**
- Design systems that minimize opportunities for error
- Decouple places where mistakes are made from places where they cause failures
- Test thoroughly at all levels
- Quick recovery: fast rollback, gradual rollouts
- Detailed monitoring: telemetry

**Scalability**
- System's ability to cope with increased load
- Not binary: "System X is scalable" is meaningless
- Ask: "If system grows in X way, how do we cope?"

**Describing Load**
- Load parameters: requests/second, read/write ratio, active users, cache hit rate
- Example: Twitter's 12K writes/sec (tweets) vs 300K reads/sec (timeline reads)
- Fan-out: number of requests to other services for one incoming request

**Describing Performance**
- Throughput: records processed per second
- Response time: time between request and response
- Latency: time request is waiting to be handled
- Use percentiles, not averages: p50, p95, p99, p999

**Percentiles in Practice**
- High percentiles (tail latencies) matter for user experience
- p99.9 might be affected by few unlucky requests
- Service Level Objectives (SLOs) and Agreements (SLAs) often use percentiles

**Approaches to Scaling**
- Vertical scaling (scale up): more powerful machine
- Horizontal scaling (scale out): more machines
- Elastic: automatically add resources when load detected
- Distributed systems have extra complexity

**Maintainability**
- Over time, many people work on system
- Three design principles:
  - **Operability**: Easy for operations to keep running smoothly
  - **Simplicity**: Easy for new engineers to understand
  - **Evolvability**: Easy to make changes

**Operability**
- Good operations: monitoring, automation, documentation, self-healing
- Good data systems: visibility into runtime behavior, standard tools integration, predictable behavior

**Simplicity**
- Complexity = accidental complexity (not inherent to problem being solved)
- Abstraction: hide implementation details
- Good abstractions reduce cognitive load

**Evolvability (Extensibility, Plasticity)**
- Agility for large-scale systems
- Simple and abstracted systems are usually easier to modify

**Chapter 2: Data Models and Query Languages**

**Relational Model**
- Data organized into relations (tables), each a collection of tuples (rows)
- Hides implementation detail behind cleaner interface
- Powerful for many-to-many relationships and joins
- Schema enforces structure

**Document Model**
- Data stored as self-contained documents (JSON, BSON)
- Better locality: all data in one place
- Schema-on-read: implicit structure, flexible
- Better for one-to-many relationships (tree structure)
- Joins are weak or nonexistent

**Relational vs Document**
- Document: better for self-contained objects, schema flexibility, locality
- Relational: better for many-to-many, joins, consistent structure
- Many databases are converging: SQL supports JSON, document DBs add joins
- Hybrid models emerging

**Graph Model**
- Vertices and edges (nodes and relationships)
- Natural for highly interconnected data
- Property graphs: vertices and edges have properties
- Examples: Neo4j, Amazon Neptune

**Query Languages**
- Declarative: describe WHAT you want, not HOW (SQL)
- Imperative: specify exact steps (most programming languages)
- Declarative is more concise, hides optimization details

**MapReduce**
- Programming model for processing large datasets
- Map: extract key-value pairs
- Reduce: combine values with same key
- Neither imperative nor declarative — somewhere between

**Chapter 3: Storage and Retrieval**

**Log-Structured Storage**
- Append-only sequence of records
- Extremely fast writes (sequential I/O)
- Read requires scanning (slow without index)

**Hash Indexes**
- In-memory hash map: key → byte offset
- Works well when all keys fit in memory
- Fast for known keys, doesn't support range queries

**SSTables and LSM-Trees**
- Sorted String Table: sorted key-value pairs
- Log-Structured Merge-Tree: multiple SSTables with compaction
- Good write throughput, compaction runs in background
- Used by: LevelDB, RocksDB, Cassandra, HBase

**B-Trees**
- Most widely used indexing structure
- Fixed-size pages (4KB), tree structure
- Balanced: O(log n) for reads and writes
- In-place updates with write-ahead log for crash recovery
- Standard in most relational databases

**LSM-Trees vs B-Trees**
- LSM: faster writes, better compression, compaction overhead
- B-Trees: faster reads, more predictable performance

**Other Indexing Structures**
- Clustered indexes: store row data within index
- Covering indexes: include some columns in index
- Multi-column indexes: concatenated or multi-dimensional
- Full-text search indexes: term dictionaries, fuzzy matching

**OLTP vs OLAP**
- OLTP: Online Transaction Processing — many short transactions
- OLAP: Online Analytical Processing — complex queries on large data
- Different access patterns, different optimizations

**Column-Oriented Storage**
- Store each column separately
- Excellent for analytics (few columns, many rows)
- Better compression (similar values grouped)
- Used by: Redshift, BigQuery, ClickHouse

**Data Warehouses**
- Separate database optimized for analytics
- ETL: Extract, Transform, Load from OLTP systems
- Star and snowflake schemas: fact tables and dimension tables

**Chapter 4: Encoding and Evolution**

**Data Encoding Formats**
- Language-specific: Python pickle, Java serialization (avoid: tied to language)
- JSON, XML: human-readable, widely supported, verbose
- Binary: more compact, faster parsing

**Thrift, Protocol Buffers, Avro**
- Schema-based binary encoding
- Compact, schema evolution support
- Code generation from schema
- Thrift and Protobuf: explicit field tags
- Avro: writer's schema and reader's schema

**Schema Evolution**
- Forward compatibility: new code reads old data
- Backward compatibility: old code reads new data
- Add optional fields for forward compatibility
- Set defaults for backward compatibility

**Modes of Dataflow**
- Databases: one process writes, another reads
- Service calls (REST, RPC): client sends request, server responds
- Message passing: asynchronous, through message broker

**REST vs RPC**
- REST: resources, HTTP verbs, stateless, human-debuggable
- RPC: looks like local function call, various protocols
- RPC abstraction is leaky — network is not like local call
- Modern RPC: gRPC (Protobuf), Finagle (Thrift)

**Message Brokers**
- Asynchronous message passing
- Decouples sender and receiver
- Durability, buffering, redelivery
- Examples: RabbitMQ, Apache Kafka

### Part II: Distributed Data

**Chapter 5: Replication**

**Why Replicate?**
- Keep data geographically close to users
- Allow continued operation if parts fail
- Scale read throughput

**Leaders and Followers**
- Leader (master): accepts writes
- Followers (slaves): replicate from leader, serve reads
- Synchronous: leader waits for follower confirmation
- Asynchronous: leader doesn't wait (potential data loss on failure)

**Handling Node Outages**
- Follower failure: catch up from leader's log
- Leader failure: failover — choose new leader, redirect clients

**Problems with Replication Lag**
- Reading your own writes (read-after-write consistency)
- Monotonic reads: don't go back in time
- Consistent prefix reads: causality preserved

**Multi-Leader Replication**
- Multiple nodes accept writes
- Better availability and performance
- Conflict resolution is hard
- Use case: multi-datacenter, offline clients

**Conflict Resolution**
- Last write wins (LWW): simple but lossy
- Merge values
- Record conflict, let application resolve
- CRDTs: conflict-free replicated data types

**Leaderless Replication**
- All nodes accept reads and writes
- Quorum: w + r > n (write nodes + read nodes > total nodes)
- Handle concurrent writes with version vectors
- Examples: Dynamo, Cassandra, Riak

**Chapter 6: Partitioning (Sharding)**

**Why Partition?**
- Dataset too big for single machine
- Query throughput too high for single machine
- Spreads data and load across many nodes

**Partitioning by Key Range**
- Each partition owns a range of keys
- Keys sorted within partition — efficient range scans
- Risk: hot spots if access isn't uniform
- Solution: add random prefix to spread load

**Partitioning by Hash of Key**
- Hash function distributes keys uniformly
- Loses ability to do efficient range queries
- Consistent hashing: minimizes data movement when adding nodes

**Secondary Indexes**
- Local index: each partition has its own
- Global index: partitioned across nodes
- Local: writes are efficient, reads are scatter-gather
- Global: reads are efficient, writes are distributed

**Rebalancing**
- Moving data when adding/removing nodes
- Don't use hash mod N: everything moves
- Fixed number of partitions: assign partitions to nodes
- Dynamic partitioning: split/merge partitions as they grow

**Request Routing**
- How do clients know which partition?
- Options: client knows, routing tier, nodes forward
- Coordination service (ZooKeeper) tracks partition assignment

**Chapter 7: Transactions**

**What Are Transactions?**
- Way to group reads and writes into logical unit
- All succeed (commit) or all fail (abort/rollback)
- Safety guarantees: don't have to worry about partial failure

**ACID**
- **Atomicity**: all or nothing, no partial failures
- **Consistency**: invariants are maintained (application's job)
- **Isolation**: concurrent transactions don't interfere
- **Durability**: committed data isn't lost

**Single-Object vs Multi-Object**
- Single-object: atomicity and isolation for one key
- Multi-object: multiple objects, multiple operations, one transaction
- Harder in distributed systems

**Weak Isolation Levels**

*Read Committed*
- No dirty reads: only see committed data
- No dirty writes: only overwrite committed data
- Most databases use this as default

*Snapshot Isolation*
- Transaction sees consistent snapshot of database
- Each transaction sees data as of start time
- Implemented with MVCC (multi-version concurrency control)

*Repeatable Read*
- Term is ambiguous — different meanings in different databases
- SQL standard definition is flawed

**Preventing Lost Updates**
- Two transactions read, modify, write — one update is lost
- Solutions: atomic operations, explicit locking, compare-and-set, conflict detection

**Write Skew and Phantoms**
- Write skew: two transactions make decisions based on same data, both write
- Phantom: transaction's query result changes because another transaction inserted
- Requires serializable isolation to prevent

**Serializability**
- Strongest isolation: result is as if transactions executed serially
- Three approaches: actual serial execution, two-phase locking, optimistic concurrency

**Actual Serial Execution**
- Really execute one at a time
- Possible with: in-memory data, fast storage, stored procedures
- Used by: Redis, VoltDB

**Two-Phase Locking (2PL)**
- Readers block writers, writers block readers
- Locks held until end of transaction
- Deadlocks possible
- Performance issues with long-running transactions

**Serializable Snapshot Isolation (SSI)**
- Optimistic: allow transactions to proceed, check at commit
- Based on snapshot isolation, detect serialization conflicts
- Better performance than 2PL for many workloads

**Chapter 8: The Trouble with Distributed Systems**

**Unreliable Networks**
- Packets can be lost, delayed, reordered, duplicated
- No way to know if message got through
- Timeouts: only way to detect failure, but slow ≠ failed

**Detecting Faults**
- Difficult to distinguish slow from dead
- Node might be dead, network might be partitioned
- None of these are certain — only probabilistic detection

**Unreliable Clocks**
- Each machine has its own quartz clock
- Clocks drift, NTP synchronization is imprecise
- Clock skew: different machines have different times

**Types of Clocks**
- Time-of-day: synchronized, can jump
- Monotonic: only goes forward, not synchronized between machines
- Use monotonic for elapsed time, be careful with time-of-day

**Process Pauses**
- Garbage collection pauses
- VM suspension
- Swapping to disk
- A process can be paused for unbounded time

**Truth Is Defined by Majority**
- Single node can't trust its own judgment
- Need quorum: majority of nodes must agree
- Leader election, lock ownership determined by quorum

**Fencing Tokens**
- When acquiring lock, get monotonically increasing token
- Include token with all operations
- Storage can reject operations with old tokens

**Byzantine Faults**
- Nodes might lie or act maliciously
- Byzantine fault tolerance: consensus despite lying nodes
- Needed for: blockchains, untrusted environments
- Not needed: typical datacenters (trust your own nodes)

**Chapter 9: Consistency and Consensus**

**Consistency Guarantees**
- Different from ACID consistency
- About replica agreement and ordering

**Linearizability**
- Strongest consistency: behaves like single copy
- Once write completes, all reads see it
- Recency guarantee: reads return most recent write
- Required for: leader election, locks, unique constraints

**Linearizability vs Serializability**
- Serializability: transactions appear to execute in some serial order
- Linearizability: single-object, real-time ordering
- Can have one without the other

**Cost of Linearizability**
- CAP theorem: during partition, choose consistency or availability
- Many systems choose availability
- Linearizability is slow (coordination required)

**Ordering Guarantees**
- Causal ordering: if A happened before B, everyone sees A before B
- Total ordering: all operations in single order everyone agrees on
- Causal is weaker than linearizable, but often sufficient

**Sequence Number Ordering**
- Assign sequence number to operations
- Single-leader: leader assigns sequence numbers
- Multi-leader/leaderless: Lamport timestamps

**Total Order Broadcast**
- Protocol for exchanging messages between nodes
- Reliable delivery: all nodes receive all messages
- Totally ordered: all nodes receive in same order
- Foundation for: database replication, serializable transactions

**Consensus**
- Getting multiple nodes to agree on something
- Required for: leader election, atomic commit, unique sequence numbers

**Consensus Algorithms**
- Paxos: classic, hard to understand, basis for many systems
- Raft: designed for understandability, used in etcd
- Zab: used by ZooKeeper

**What Consensus Provides**
- Uniform agreement: all nodes decide same value
- Integrity: no node decides twice
- Validity: value decided was proposed by some node
- Termination: all non-crashed nodes eventually decide

**Coordination Services**
- ZooKeeper, etcd, Consul
- Provide: consensus, failure detection, change notification
- Use for: leader election, service discovery, distributed locks
- Small amount of data, replicated across all nodes

### Part III: Derived Data

**Chapter 10: Batch Processing**

**Unix Philosophy**
- Make each program do one thing well
- Expect output of every program to become input to another
- Composability: small programs combined into pipelines
- Uniform interface: text streams

**MapReduce**
- Programming model for processing large datasets
- Map: extract key-value pairs from input
- Shuffle: sort and group by key
- Reduce: combine values for each key

**MapReduce vs Unix**
- Similar philosophy: compose simple tools
- Scale: MapReduce distributes across cluster
- HDFS: distributed filesystem for input/output

**Beyond MapReduce**
- MapReduce is low-level, lots of boilerplate
- Higher-level abstractions: Hive (SQL), Pig, Cascading
- Dataflow engines: Spark, Flink, Tez

**Dataflow Engines**
- Model computation as directed acyclic graph (DAG)
- Operators connected by data flowing between them
- More flexible than map-reduce-map-reduce pattern
- In-memory processing, avoid writing to disk

**Graphs and Iterative Processing**
- MapReduce doesn't handle iterative algorithms well
- Graph processing: PageRank, social network analysis
- Bulk Synchronous Parallel (BSP): think like a vertex
- Pregel model: send messages along edges

**Chapter 11: Stream Processing**

**Why Stream Processing?**
- Batch processing has high latency (process yesterday's data)
- Some applications need faster: fraud detection, monitoring
- Event streams: continuous flow of data

**Messaging Systems**
- Direct messaging: UDP multicast, ZeroMQ
- Message brokers: RabbitMQ, Amazon SQS
- Log-based: Apache Kafka, Amazon Kinesis

**Log-Based Message Brokers**
- Append-only log of messages
- Consumers track position (offset) in log
- Messages retained for days/weeks
- Replay possible: rewind to earlier offset

**Databases and Streams**
- Change Data Capture (CDC): capture changes as stream
- Event sourcing: store events, not current state
- Derive views from event log
- Immutable events: append-only, never modify

**Processing Streams**

*Uses of Stream Processing*
- Complex event processing (CEP): pattern matching
- Stream analytics: real-time dashboards, metrics
- Materialized views: maintain derived data
- Search: full-text search on stream
- Message passing: inter-service communication

*Reasoning About Time*
- Event time: when event occurred
- Processing time: when event is processed
- Watermarks: estimate of event time progress
- Late arrivals: events that arrive after their time window

*Stream Joins*
- Stream-stream: join events from two streams by time window
- Stream-table: enrich stream events with database lookup
- Table-table: CDC changes to both tables

*Fault Tolerance*
- Exactly-once semantics is hard
- Microbatching: small batch jobs (Spark Streaming)
- Checkpointing: periodic snapshots of state
- Transactions: atomic commit of state updates

**Chapter 12: The Future of Data Systems**

**Data Integration**
- No single tool can do everything well
- Combine specialized tools: OLTP + OLAP + search + cache
- Derived data: transform and load between systems
- Total ordering of writes helps keep derived data consistent

**Unbundling Databases**
- Traditional databases bundle: storage, indexes, query engine
- Separate into: log (source of truth) + derived views
- Build custom "database" from components

**Designing Applications Around Dataflow**
- Application state is derived from event log
- Materialized views maintained by stream processing
- Separation: write path (eager) vs read path (lazy)

**Observing Derived State**
- Push data to clients (WebSockets, server-sent events)
- Read-after-write consistency without coordination
- End-to-end argument: some guarantees must be at application level

**Correctness**
- Exactly-once semantics: operation is executed once, even if it fails and retries
- Idempotence: operation can be applied multiple times with same result
- End-to-end exactly-once: from user action to final effect

**Timeliness and Integrity**
- Timeliness: users see up-to-date state
- Integrity: data is not corrupted
- Can have integrity without timeliness (eventual consistency)
- Integrity is more important: corruption is hard to fix

**Trust but Verify**
- Bugs happen, hardware fails, people make mistakes
- Design for auditability
- Self-validating systems: checksums, reconciliation

**Doing the Right Thing**
- Data systems have power and responsibility
- Privacy: users own their data
- Tracking, surveillance, predictive analytics have ethical implications
- Consider societal effects of systems we build

---

## QUICK CHECKLISTS

### Before Writing Code
- [ ] Do I understand the requirement?
- [ ] What's the simplest solution?
- [ ] What could go wrong?
- [ ] How will this scale?
- [ ] What are the edge cases?

### During Code Review
- [ ] Are names clear and intention-revealing?
- [ ] Are functions small and focused?
- [ ] Is there duplication (DRY)?
- [ ] Are there side effects or hidden state?
- [ ] Are edge cases handled?
- [ ] Are there tests?
- [ ] Does it follow project conventions?
- [ ] Is error handling appropriate?

### For Data Systems
- [ ] What are the access patterns?
- [ ] What consistency is actually needed?
- [ ] How will this scale?
- [ ] What happens when X fails?
- [ ] Is this OLTP or OLAP?
- [ ] How is data partitioned?
- [ ] What's the replication strategy?

### For Distributed Systems
- [ ] What if the network partitions?
- [ ] What if messages are delayed or lost?
- [ ] What if clocks are skewed?
- [ ] What if a node crashes mid-operation?
- [ ] Do we need consensus?
- [ ] What's the consistency model?

### For Production
- [ ] Is it observable (logging, metrics, tracing)?
- [ ] Is it secure (auth, validation, encryption)?
- [ ] Is it documented?
- [ ] Is it tested (unit, integration, e2e)?
- [ ] Can it be deployed and rolled back safely?
- [ ] What's the on-call playbook?

---

## DOMAIN-DRIVEN DESIGN (Eric Evans)

### Strategic Design

**Bounded Context**
- A Bounded Context is a semantic boundary within which a particular domain model applies
- Each context has its own Ubiquitous Language — the same word may mean different things in different contexts
- Example: "Customer" in Sales context vs Support context vs Billing context
- Explicitly define the boundaries — don't let the model leak across contexts

**Ubiquitous Language**
- A shared vocabulary between developers and domain experts
- Used in code, documentation, and conversations
- If the language is awkward, the model is wrong
- Refine the language as understanding deepens

**Context Mapping**

| Pattern | Description | When to Use |
|---------|-------------|-------------|
| **Shared Kernel** | Two contexts share a subset of the model | Small teams, tight coordination |
| **Customer/Supplier** | Upstream team provides, downstream consumes | Clear dependency direction |
| **Conformist** | Downstream adopts upstream's model as-is | No negotiating power |
| **Anti-Corruption Layer** | Translation layer between contexts | Protecting your model from legacy/external |
| **Open Host Service** | Expose well-documented protocol | Multiple consumers |
| **Published Language** | Use a well-documented interchange language | Industry standard protocols |
| **Separate Ways** | No integration, duplicate if needed | Integration cost too high |
| **Partnership** | Two teams coordinate bidirectionally | Mutual dependency, same organization |

**Context Map Example**
```
┌─────────────────────────────────────────────────────────┐
│                    E-Commerce System                     │
├─────────────────────────────────────────────────────────┤
│                                                          │
│  ┌──────────┐    Customer/     ┌──────────────┐         │
│  │  Sales   │ ◄──Supplier────► │   Inventory  │         │
│  │ Context  │                  │   Context    │         │
│  └────┬─────┘                  └──────────────┘         │
│       │                                                  │
│       │ Shared Kernel (Product ID, Customer ID)         │
│       │                                                  │
│  ┌────▼─────┐                  ┌──────────────┐         │
│  │ Billing  │ ◄───ACL─────────│   Legacy     │         │
│  │ Context  │                  │   ERP        │         │
│  └──────────┘                  └──────────────┘         │
│                                                          │
└─────────────────────────────────────────────────────────┘
```

### Tactical Design

**Entities**
- Objects with continuous identity that spans the lifetime of the system
- Identity, not attributes, defines equality
- Track changes over time
- Example: User, Order, Account

```python
class User:
    def __init__(self, user_id: UserId, email: Email, name: Name):
        self._id = user_id  # Identity
        self._email = email
        self._name = name
        self._created_at = datetime.now()

    def __eq__(self, other):
        if not isinstance(other, User):
            return False
        return self._id == other._id  # Identity-based equality

    def change_email(self, new_email: Email) -> None:
        # Business logic for changing email
        self._email = new_email
```

**Value Objects**
- Objects defined by their attributes, not identity
- Immutable — replace, don't modify
- No identity — two value objects with same attributes are equal
- Examples: Money, Address, DateRange, Email

```python
@dataclass(frozen=True)  # Immutable
class Money:
    amount: Decimal
    currency: str

    def add(self, other: 'Money') -> 'Money':
        if self.currency != other.currency:
            raise ValueError("Cannot add different currencies")
        return Money(self.amount + other.amount, self.currency)

    def __eq__(self, other):
        return self.amount == other.amount and self.currency == other.currency
```

**Aggregates**
- Cluster of entities and value objects treated as a unit
- Has a single root entity (Aggregate Root)
- All external references go through the root
- Ensures invariants within the boundary
- Transaction boundary — changes are atomic within an aggregate

```python
class Order:  # Aggregate Root
    def __init__(self, order_id: OrderId, customer_id: CustomerId):
        self._id = order_id
        self._customer_id = customer_id
        self._items: List[OrderItem] = []  # Only accessible through Order
        self._status = OrderStatus.DRAFT

    def add_item(self, product_id: ProductId, quantity: int, price: Money) -> None:
        if self._status != OrderStatus.DRAFT:
            raise InvalidOperationError("Cannot add items to submitted order")
        # Invariant: max 50 items per order
        if len(self._items) >= 50:
            raise DomainError("Order cannot have more than 50 items")
        self._items.append(OrderItem(product_id, quantity, price))

    def submit(self) -> None:
        if not self._items:
            raise DomainError("Cannot submit empty order")
        self._status = OrderStatus.SUBMITTED
```

**Aggregate Design Rules**
1. Reference other aggregates by ID only
2. Keep aggregates small — large aggregates cause contention
3. Modify one aggregate per transaction
4. Use eventual consistency between aggregates
5. Aggregate boundaries often align with transaction boundaries

**Repositories**
- Abstraction for aggregate persistence
- Collection-like interface for retrieving and storing aggregates
- One repository per aggregate root
- Hides storage details from domain

```python
class OrderRepository(ABC):
    @abstractmethod
    def find_by_id(self, order_id: OrderId) -> Optional[Order]:
        pass

    @abstractmethod
    def save(self, order: Order) -> None:
        pass

    @abstractmethod
    def find_by_customer(self, customer_id: CustomerId) -> List[Order]:
        pass

# Implementation
class PostgresOrderRepository(OrderRepository):
    def find_by_id(self, order_id: OrderId) -> Optional[Order]:
        row = self._db.query("SELECT * FROM orders WHERE id = %s", order_id)
        return self._to_aggregate(row) if row else None
```

**Domain Services**
- Operations that don't naturally belong to an entity or value object
- Stateless operations involving multiple aggregates
- Named using ubiquitous language verbs

```python
class PaymentService:  # Domain Service
    def __init__(self,
                 order_repo: OrderRepository,
                 payment_gateway: PaymentGateway):
        self._order_repo = order_repo
        self._gateway = payment_gateway

    def process_payment(self, order_id: OrderId, payment_method: PaymentMethod) -> PaymentResult:
        order = self._order_repo.find_by_id(order_id)
        if not order:
            raise OrderNotFound(order_id)

        # Cross-aggregate operation
        result = self._gateway.charge(payment_method, order.total())
        if result.success:
            order.mark_paid()
            self._order_repo.save(order)

        return result
```

**Domain Events**
- Something that happened in the domain that domain experts care about
- Named in past tense: OrderPlaced, PaymentReceived, InventoryDepleted
- Immutable record of what happened
- Enable loose coupling between aggregates

```python
@dataclass(frozen=True)
class OrderPlaced:
    order_id: OrderId
    customer_id: CustomerId
    total: Money
    occurred_at: datetime

    @classmethod
    def from_order(cls, order: Order) -> 'OrderPlaced':
        return cls(
            order_id=order.id,
            customer_id=order.customer_id,
            total=order.total(),
            occurred_at=datetime.now()
        )

class Order:
    def submit(self) -> List[DomainEvent]:
        if not self._items:
            raise DomainError("Cannot submit empty order")
        self._status = OrderStatus.SUBMITTED
        return [OrderPlaced.from_order(self)]  # Return events
```

### Event Sourcing

**Concept**
- Store state as sequence of events, not current state
- Current state = replay all events from the beginning
- Events are append-only, immutable
- Complete audit trail

**Event Store Pattern**
```python
class EventStore:
    def append(self, stream_id: str, events: List[DomainEvent],
               expected_version: int) -> None:
        """Append events with optimistic concurrency check"""
        pass

    def read(self, stream_id: str) -> List[DomainEvent]:
        """Read all events for a stream"""
        pass

class EventSourcedOrder:
    def __init__(self, events: List[DomainEvent]):
        self._id = None
        self._items = []
        self._status = None
        # Replay events to rebuild state
        for event in events:
            self._apply(event)

    def _apply(self, event: DomainEvent) -> None:
        if isinstance(event, OrderCreated):
            self._id = event.order_id
            self._status = OrderStatus.DRAFT
        elif isinstance(event, ItemAdded):
            self._items.append(event.item)
        elif isinstance(event, OrderSubmitted):
            self._status = OrderStatus.SUBMITTED
```

**Snapshots**
- Periodically save current state to speed up rebuilding
- Snapshot + events after snapshot = current state
- Trade-off: storage vs rebuild time

### CQRS (Command Query Responsibility Segregation)

**Concept**
- Separate models for reading and writing
- Command model: handles writes, enforces invariants
- Query model: optimized for reads, denormalized
- Often combined with Event Sourcing

```
┌─────────────────────────────────────────────────────────┐
│                                                          │
│   User ────► Command ────► Write Model ────► Event Store │
│              Handler        (Domain)          (Source)   │
│                                    │                     │
│                                    ▼                     │
│   User ◄──── Query  ◄──── Read Model ◄──── Projector    │
│              Handler      (Denormalized)                 │
│                                                          │
└─────────────────────────────────────────────────────────┘
```

**When to Use CQRS**
- Different read/write patterns
- Read model needs different shape than write model
- High read-to-write ratio
- Complex domain that benefits from event sourcing

**When NOT to Use**
- Simple CRUD applications
- Same data shape for reads and writes
- Small teams, simple domains

### Anti-Corruption Layer

**Purpose**
- Protect your domain model from external/legacy systems
- Translate between your ubiquitous language and external models
- Isolate integration complexity

```python
# External legacy system uses different model
class LegacyCustomerService:
    def get_cust_data(self, cust_num: str) -> dict:
        return {"cust_num": "123", "nm": "John", "addr_1": "123 Main St"}

# Anti-Corruption Layer
class CustomerAntiCorruptionLayer:
    def __init__(self, legacy: LegacyCustomerService):
        self._legacy = legacy

    def find_customer(self, customer_id: CustomerId) -> Optional[Customer]:
        legacy_data = self._legacy.get_cust_data(str(customer_id))
        if not legacy_data:
            return None

        # Translate to our domain model
        return Customer(
            customer_id=CustomerId(legacy_data["cust_num"]),
            name=Name(legacy_data["nm"]),
            address=Address.from_legacy(legacy_data)
        )
```

---

## REFACTORING (Martin Fowler)

### Code Smells Reference

**Bloaters** — Code that grows too large

| Smell | Symptoms | Refactoring |
|-------|----------|-------------|
| Long Method | Method > 10-20 lines, does multiple things | Extract Method, Replace Temp with Query |
| Large Class | Class with too many responsibilities | Extract Class, Extract Subclass |
| Primitive Obsession | Using primitives instead of small objects | Replace Primitive with Object, Introduce Parameter Object |
| Long Parameter List | > 3-4 parameters | Introduce Parameter Object, Preserve Whole Object |
| Data Clumps | Same group of data appears together repeatedly | Extract Class, Introduce Parameter Object |

**Object-Orientation Abusers**

| Smell | Symptoms | Refactoring |
|-------|----------|-------------|
| Switch Statements | Same switch on type in multiple places | Replace Conditional with Polymorphism |
| Temporary Field | Instance variable only used in some scenarios | Extract Class, Introduce Null Object |
| Refused Bequest | Subclass doesn't use inherited methods | Replace Inheritance with Delegation |
| Alternative Classes with Different Interfaces | Classes do the same thing with different signatures | Rename Method, Extract Superclass |

**Change Preventers**

| Smell | Symptoms | Refactoring |
|-------|----------|-------------|
| Divergent Change | One class changed for multiple reasons | Extract Class |
| Shotgun Surgery | One change requires edits to many classes | Move Method, Move Field, Inline Class |
| Parallel Inheritance Hierarchies | Creating subclass requires creating another subclass | Move Method, Move Field |

**Dispensables**

| Smell | Symptoms | Refactoring |
|-------|----------|-------------|
| Comments | Code needs extensive comments to explain | Extract Method, Rename, Introduce Assertion |
| Duplicate Code | Same code in multiple places | Extract Method, Pull Up Method, Form Template Method |
| Lazy Class | Class that doesn't do enough | Inline Class, Collapse Hierarchy |
| Data Class | Class with only fields and getters/setters | Move Method, Encapsulate Field, Hide Method |
| Dead Code | Unused code | Delete it |
| Speculative Generality | "We might need this someday" | Collapse Hierarchy, Inline Class, Remove Parameter |

**Couplers**

| Smell | Symptoms | Refactoring |
|-------|----------|-------------|
| Feature Envy | Method uses another class's data extensively | Move Method |
| Inappropriate Intimacy | Two classes know too much about each other | Move Method, Move Field, Extract Class |
| Message Chains | a.getB().getC().getD().doSomething() | Hide Delegate, Extract Method |
| Middle Man | Class only delegates to another class | Remove Middle Man, Inline Method |

### Refactoring Catalog

**Composing Methods**

*Extract Method*
```python
# Before
def print_invoice(invoice):
    print("================")
    print("Customer Invoice")
    print("================")
    total = 0
    for item in invoice.items:
        print(f"{item.name}: ${item.price}")
        total += item.price
    print(f"Total: ${total}")

# After
def print_invoice(invoice):
    print_banner()
    print_items(invoice.items)
    print_total(calculate_total(invoice.items))

def print_banner():
    print("================")
    print("Customer Invoice")
    print("================")

def print_items(items):
    for item in items:
        print(f"{item.name}: ${item.price}")

def calculate_total(items):
    return sum(item.price for item in items)

def print_total(total):
    print(f"Total: ${total}")
```

*Replace Temp with Query*
```python
# Before
def calculate_price(quantity, item_price):
    base_price = quantity * item_price
    if base_price > 1000:
        return base_price * 0.95
    return base_price * 0.98

# After
def calculate_price(quantity, item_price):
    if base_price(quantity, item_price) > 1000:
        return base_price(quantity, item_price) * 0.95
    return base_price(quantity, item_price) * 0.98

def base_price(quantity, item_price):
    return quantity * item_price
```

*Introduce Explaining Variable*
```python
# Before
if platform.upper().find("MAC") > -1 and \
   browser.upper().find("IE") > -1 and \
   was_initialized() and resize > 0:
    # do something

# After
is_mac_os = platform.upper().find("MAC") > -1
is_ie_browser = browser.upper().find("IE") > -1
was_resized = resize > 0

if is_mac_os and is_ie_browser and was_initialized() and was_resized:
    # do something
```

**Moving Features Between Objects**

*Move Method*
```python
# Before — Feature Envy
class Order:
    def discount_for(self, customer):
        if customer.loyalty_points > 1000:
            return 0.10
        elif customer.loyalty_points > 500:
            return 0.05
        return 0

# After — Move to where data lives
class Customer:
    def discount_rate(self):
        if self.loyalty_points > 1000:
            return 0.10
        elif self.loyalty_points > 500:
            return 0.05
        return 0

class Order:
    def discount_for(self, customer):
        return customer.discount_rate()
```

*Extract Class*
```python
# Before — Class with multiple responsibilities
class Person:
    def __init__(self, name, area_code, number, street, city, zip_code):
        self.name = name
        self.area_code = area_code
        self.number = number
        self.street = street
        self.city = city
        self.zip_code = zip_code

    def phone_number(self):
        return f"({self.area_code}) {self.number}"

    def full_address(self):
        return f"{self.street}, {self.city} {self.zip_code}"

# After — Cohesive classes
class PhoneNumber:
    def __init__(self, area_code, number):
        self.area_code = area_code
        self.number = number

    def __str__(self):
        return f"({self.area_code}) {self.number}"

class Address:
    def __init__(self, street, city, zip_code):
        self.street = street
        self.city = city
        self.zip_code = zip_code

    def __str__(self):
        return f"{self.street}, {self.city} {self.zip_code}"

class Person:
    def __init__(self, name, phone: PhoneNumber, address: Address):
        self.name = name
        self.phone = phone
        self.address = address
```

**Simplifying Conditional Expressions**

*Decompose Conditional*
```python
# Before
if date.before(SUMMER_START) or date.after(SUMMER_END):
    charge = quantity * winter_rate + winter_service_charge
else:
    charge = quantity * summer_rate

# After
if is_winter(date):
    charge = winter_charge(quantity)
else:
    charge = summer_charge(quantity)

def is_winter(date):
    return date.before(SUMMER_START) or date.after(SUMMER_END)

def winter_charge(quantity):
    return quantity * winter_rate + winter_service_charge

def summer_charge(quantity):
    return quantity * summer_rate
```

*Replace Conditional with Polymorphism*
```python
# Before
class Employee:
    def calculate_pay(self):
        if self.type == "engineer":
            return self.base_salary * 1.2
        elif self.type == "salesperson":
            return self.base_salary + self.commission
        elif self.type == "manager":
            return self.base_salary * 1.5 + self.bonus

# After
class Employee:
    def calculate_pay(self):
        raise NotImplementedError

class Engineer(Employee):
    def calculate_pay(self):
        return self.base_salary * 1.2

class Salesperson(Employee):
    def calculate_pay(self):
        return self.base_salary + self.commission

class Manager(Employee):
    def calculate_pay(self):
        return self.base_salary * 1.5 + self.bonus
```

*Introduce Null Object*
```python
# Before — Null checks everywhere
class Customer:
    pass

def get_customer(id):
    return customer_db.get(id)  # Returns None if not found

# Usage (fragile)
customer = get_customer(id)
if customer:
    name = customer.name
else:
    name = "Guest"

# After — Null Object
class NullCustomer:
    name = "Guest"

    def is_null(self):
        return True

def get_customer(id):
    customer = customer_db.get(id)
    return customer if customer else NullCustomer()

# Usage (robust)
customer = get_customer(id)
name = customer.name  # Works for both real and null customers
```

*Replace Nested Conditional with Guard Clauses*
```python
# Before — Deeply nested
def calculate_pay(employee):
    if employee.is_dead:
        result = dead_amount()
    else:
        if employee.is_separated:
            result = separated_amount()
        else:
            if employee.is_retired:
                result = retired_amount()
            else:
                result = normal_pay_amount()
    return result

# After — Guard clauses
def calculate_pay(employee):
    if employee.is_dead:
        return dead_amount()
    if employee.is_separated:
        return separated_amount()
    if employee.is_retired:
        return retired_amount()
    return normal_pay_amount()
```

**Making Method Calls Simpler**

*Introduce Parameter Object*
```python
# Before
def amount_invoiced(start_date, end_date):
    pass

def amount_received(start_date, end_date):
    pass

def amount_overdue(start_date, end_date):
    pass

# After
@dataclass
class DateRange:
    start: date
    end: date

    def includes(self, date):
        return self.start <= date <= self.end

def amount_invoiced(range: DateRange):
    pass

def amount_received(range: DateRange):
    pass

def amount_overdue(range: DateRange):
    pass
```

*Replace Error Code with Exception*
```python
# Before
def withdraw(amount):
    if amount > self.balance:
        return -1  # Error code
    self.balance -= amount
    return 0  # Success

# After
class InsufficientFundsError(Exception):
    pass

def withdraw(amount):
    if amount > self.balance:
        raise InsufficientFundsError(f"Balance: {self.balance}, Requested: {amount}")
    self.balance -= amount
```

### Big Refactorings

**Tease Apart Inheritance**
- When inheritance hierarchy is doing two jobs at once
- Create two separate hierarchies with delegation between them

**Convert Procedural Design to Objects**
- Identify data clumps and their procedures
- Move procedures to the classes containing the data
- Use Extract Method to clean up long procedures

**Separate Domain from Presentation**
- Domain logic shouldn't depend on UI
- Extract domain classes that can be tested independently
- Use Observer pattern for domain to notify UI

**Extract Hierarchy**
- When one class does too much with conditionals
- Create subclasses for each conditional branch
- Move logic to subclasses using polymorphism

---

## MICROSERVICES PATTERNS

### Decomposition Patterns

**Decompose by Business Capability**
- Align services with business capabilities (what the business does)
- Example: Order Management, Inventory, Shipping, Payments
- Stable boundaries — business capabilities don't change frequently
- Each service has its own team

**Decompose by Subdomain**
- Use DDD to identify bounded contexts
- Core Domain: competitive advantage, most important
- Supporting Subdomain: necessary but not differentiating
- Generic Subdomain: can be outsourced/bought

**Strangler Fig Pattern**
- Gradually migrate from monolith to microservices
- New features in microservices
- Incrementally extract features from monolith
- Facade routes to old or new implementation

```
┌────────────────────────────────────────────────┐
│                   Facade                        │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐        │
│  │Feature A│  │Feature B│  │Feature C│        │
│  │  (new)  │  │  (new)  │  │ (old)   │        │
│  └────┬────┘  └────┬────┘  └────┬────┘        │
│       ▼            ▼            ▼              │
│  ┌─────────┐  ┌─────────┐  ┌───────────────┐  │
│  │ Service │  │ Service │  │   Monolith    │  │
│  │    A    │  │    B    │  │               │  │
│  └─────────┘  └─────────┘  └───────────────┘  │
└────────────────────────────────────────────────┘
```

### Communication Patterns

**Synchronous Communication**

| Pattern | Description | Use When |
|---------|-------------|----------|
| REST | HTTP-based, resource-oriented | Public APIs, web clients |
| gRPC | Binary protocol, strongly typed | Internal services, high performance |
| GraphQL | Query language, client specifies data | Multiple clients, different data needs |

**Asynchronous Communication**

| Pattern | Description | Use When |
|---------|-------------|----------|
| Message Queue | Point-to-point, message consumed once | Task distribution |
| Pub/Sub | Message delivered to all subscribers | Event broadcasting |
| Event Streaming | Ordered log of events | Event sourcing, replay needed |

**API Gateway Pattern**
```
┌─────────────────────────────────────────────────┐
│                    Clients                       │
│   Web App    Mobile App    Partner API          │
└──────┬──────────┬──────────────┬────────────────┘
       │          │              │
       ▼          ▼              ▼
┌─────────────────────────────────────────────────┐
│               API Gateway                        │
│  • Authentication      • Rate Limiting          │
│  • Request Routing     • Load Balancing         │
│  • Protocol Translation • Caching               │
└────────┬────────────────┬──────────────┬────────┘
         │                │              │
    ┌────▼────┐     ┌────▼────┐    ┌────▼────┐
    │Service A│     │Service B│    │Service C│
    └─────────┘     └─────────┘    └─────────┘
```

### Data Management Patterns

**Database per Service**
- Each service owns its data
- No direct database access between services
- Loose coupling — service can change schema independently
- Challenge: distributed queries, data consistency

**Saga Pattern**
- Manage transactions across multiple services
- Sequence of local transactions
- Each step publishes event triggering next step
- Compensating transactions for rollback

*Choreography Saga*
```
┌─────────┐    ┌──────────┐    ┌─────────┐    ┌─────────┐
│  Order  │───►│ Inventory│───►│ Payment │───►│Shipping │
│ Service │◄───│ Service  │◄───│ Service │◄───│ Service │
└─────────┘    └──────────┘    └─────────┘    └─────────┘
   Events        Events          Events         Events
```

*Orchestration Saga*
```
                    ┌────────────┐
                    │   Saga     │
                    │Orchestrator│
                    └──────┬─────┘
           ┌───────────────┼───────────────┐
           ▼               ▼               ▼
     ┌──────────┐    ┌─────────┐    ┌─────────┐
     │ Inventory│    │ Payment │    │Shipping │
     │ Service  │    │ Service │    │ Service │
     └──────────┘    └─────────┘    └─────────┘
```

**CQRS for Microservices**
- Separate read and write models across services
- Read service optimized for queries
- Write service handles commands and emits events
- Eventually consistent

### Resilience Patterns

**Circuit Breaker**
```python
class CircuitBreaker:
    def __init__(self, failure_threshold=5, timeout=60):
        self.failure_count = 0
        self.failure_threshold = failure_threshold
        self.timeout = timeout
        self.state = "CLOSED"  # CLOSED, OPEN, HALF_OPEN
        self.last_failure_time = None

    def call(self, func, *args, **kwargs):
        if self.state == "OPEN":
            if self._should_try_again():
                self.state = "HALF_OPEN"
            else:
                raise CircuitOpenError()

        try:
            result = func(*args, **kwargs)
            self._on_success()
            return result
        except Exception as e:
            self._on_failure()
            raise

    def _on_success(self):
        self.failure_count = 0
        self.state = "CLOSED"

    def _on_failure(self):
        self.failure_count += 1
        self.last_failure_time = time.time()
        if self.failure_count >= self.failure_threshold:
            self.state = "OPEN"
```

**Retry with Exponential Backoff**
```python
def retry_with_backoff(func, max_retries=3, base_delay=1):
    for attempt in range(max_retries):
        try:
            return func()
        except RetryableError:
            if attempt == max_retries - 1:
                raise
            delay = base_delay * (2 ** attempt) + random.uniform(0, 1)
            time.sleep(delay)
```

**Bulkhead Pattern**
- Isolate resources to prevent cascading failures
- Separate thread pools, connection pools per service
- Failure in one doesn't exhaust resources for others

### Deployment Patterns

**Blue-Green Deployment**
```
┌────────────────────────────────────────────────┐
│                 Load Balancer                   │
│                      │                          │
│          ┌──────────┴──────────┐               │
│          ▼                     ▼               │
│    ┌──────────┐          ┌──────────┐          │
│    │  Blue    │          │  Green   │          │
│    │ (v1.0)   │          │ (v1.1)   │          │
│    │ ACTIVE   │          │ STANDBY  │          │
│    └──────────┘          └──────────┘          │
│                                                 │
│    After verification, switch traffic to Green │
└────────────────────────────────────────────────┘
```

**Canary Deployment**
```
┌────────────────────────────────────────────────┐
│              Load Balancer (Weighted)          │
│                      │                          │
│          ┌──────────┴──────────┐               │
│          ▼ (95%)               ▼ (5%)          │
│    ┌──────────┐          ┌──────────┐          │
│    │  Stable  │          │  Canary  │          │
│    │ (v1.0)   │          │ (v1.1)   │          │
│    └──────────┘          └──────────┘          │
│                                                 │
│    Gradually increase canary traffic           │
└────────────────────────────────────────────────┘
```

**Feature Flags**
```python
class FeatureFlags:
    def is_enabled(self, feature: str, user_id: str = None) -> bool:
        flag = self._get_flag(feature)
        if not flag:
            return False

        # Percentage rollout
        if flag.rollout_percentage < 100:
            if hash(user_id) % 100 >= flag.rollout_percentage:
                return False

        # User targeting
        if flag.target_users and user_id not in flag.target_users:
            return False

        return flag.enabled

# Usage
if feature_flags.is_enabled("new_checkout", user.id):
    return new_checkout_flow()
else:
    return legacy_checkout_flow()
```

### Service Mesh

**What is a Service Mesh?**
- Infrastructure layer handling service-to-service communication
- Sidecar proxy alongside each service instance
- Provides: traffic management, security, observability

**Service Mesh Architecture (Istio)**
```
┌────────────────────────────────────────────────┐
│                 Control Plane                   │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐        │
│  │ Istiod  │  │ Config  │  │  Cert   │        │
│  │(Pilot)  │  │ (Galley)│  │ (Citadel)│        │
│  └────┬────┘  └────┬────┘  └────┬────┘        │
│       └────────────┴────────────┘              │
│                     │                          │
├─────────────────────┼──────────────────────────┤
│    Data Plane       │                          │
│                     ▼                          │
│  ┌─────────────────────────────────────────┐  │
│  │     Pod                                  │  │
│  │  ┌─────────┐    ┌─────────────────────┐ │  │
│  │  │ Service │◄──►│   Envoy Sidecar     │ │  │
│  │  │ A       │    │   (Traffic mgmt,    │ │  │
│  │  └─────────┘    │    mTLS, metrics)   │ │  │
│  │                 └─────────────────────┘ │  │
│  └─────────────────────────────────────────┘  │
└────────────────────────────────────────────────┘
```

---

## OBSERVABILITY

### The Three Pillars

**Logs**
- Record of discrete events
- Structured (JSON) preferred over unstructured
- Include: timestamp, level, message, correlation ID, context

**Metrics**
- Numeric measurements over time
- Aggregated, low cardinality
- Types: counters, gauges, histograms

**Traces**
- Request flow across services
- Spans represent operations
- Correlation via trace ID and span ID

### Structured Logging

**JSON Log Format**
```json
{
  "timestamp": "2024-01-15T10:30:45.123Z",
  "level": "INFO",
  "logger": "com.app.OrderService",
  "message": "Order placed successfully",
  "trace_id": "abc123",
  "span_id": "def456",
  "user_id": "user-789",
  "order_id": "ord-001",
  "amount": 99.99,
  "duration_ms": 45
}
```

**Correlation IDs**
```python
import uuid
from contextvars import ContextVar

correlation_id: ContextVar[str] = ContextVar('correlation_id')

class CorrelationMiddleware:
    async def __call__(self, request, call_next):
        # Get from header or generate new
        corr_id = request.headers.get('X-Correlation-ID', str(uuid.uuid4()))
        correlation_id.set(corr_id)

        response = await call_next(request)
        response.headers['X-Correlation-ID'] = corr_id
        return response

class StructuredLogger:
    def info(self, message: str, **kwargs):
        log_entry = {
            "timestamp": datetime.utcnow().isoformat(),
            "level": "INFO",
            "message": message,
            "correlation_id": correlation_id.get(None),
            **kwargs
        }
        print(json.dumps(log_entry))
```

### Distributed Tracing

**OpenTelemetry Concepts**
```
Trace: [─────────────────────────────────────────────────]
  │
  ├─ Span A (API Gateway): [──────────────────────────────]
  │    │
  │    ├─ Span B (Auth Service): [────]
  │    │
  │    └─ Span C (Order Service): [───────────────────────]
  │         │
  │         ├─ Span D (Inventory): [─────]
  │         │
  │         └─ Span E (Payment): [────────────]
```

**OpenTelemetry Implementation**
```python
from opentelemetry import trace
from opentelemetry.sdk.trace import TracerProvider
from opentelemetry.sdk.trace.export import BatchSpanProcessor
from opentelemetry.exporter.otlp.proto.grpc.trace_exporter import OTLPSpanExporter

# Setup
provider = TracerProvider()
processor = BatchSpanProcessor(OTLPSpanExporter(endpoint="localhost:4317"))
provider.add_span_processor(processor)
trace.set_tracer_provider(provider)

tracer = trace.get_tracer(__name__)

# Usage
@tracer.start_as_current_span("process_order")
def process_order(order_id: str):
    current_span = trace.get_current_span()
    current_span.set_attribute("order_id", order_id)

    with tracer.start_as_current_span("validate_inventory") as span:
        span.set_attribute("product_count", len(order.items))
        check_inventory(order)

    with tracer.start_as_current_span("process_payment"):
        charge_customer(order)
```

**Context Propagation**
```python
from opentelemetry.propagate import inject, extract

# Outgoing request — inject context
def call_external_service(url, data):
    headers = {}
    inject(headers)  # Adds trace context headers
    return requests.post(url, json=data, headers=headers)

# Incoming request — extract context
def handle_request(request):
    context = extract(request.headers)
    with tracer.start_as_current_span("handle_request", context=context):
        # Process request
        pass
```

### Metrics

**RED Method (Request-focused)**
- **R**ate: requests per second
- **E**rrors: failed requests per second
- **D**uration: response time distribution

**USE Method (Resource-focused)**
- **U**tilization: percentage of resource busy
- **S**aturation: work queued (can't be serviced)
- **E**rrors: error events

**Golden Signals (SRE)**
- Latency
- Traffic
- Errors
- Saturation

**Metrics Implementation**
```python
from prometheus_client import Counter, Histogram, Gauge

# Counters — only go up
http_requests_total = Counter(
    'http_requests_total',
    'Total HTTP requests',
    ['method', 'endpoint', 'status']
)

# Histograms — distribution of values
request_duration_seconds = Histogram(
    'request_duration_seconds',
    'Request latency',
    ['method', 'endpoint'],
    buckets=[0.01, 0.05, 0.1, 0.5, 1.0, 5.0]
)

# Gauges — can go up or down
active_connections = Gauge(
    'active_connections',
    'Number of active connections'
)

# Usage
@request_duration_seconds.labels(method='GET', endpoint='/orders').time()
def get_orders():
    http_requests_total.labels(method='GET', endpoint='/orders', status='200').inc()
    return orders
```

### SLIs, SLOs, and SLAs

**Service Level Indicator (SLI)**
- Quantitative measure of service behavior
- Example: "99.5% of requests complete in under 200ms"

**Service Level Objective (SLO)**
- Target value for an SLI
- Example: "99.9% availability over 30 days"

**Service Level Agreement (SLA)**
- Contract with consequences for not meeting SLOs
- Example: "99.9% uptime or credits applied"

**Error Budget**
```
Error Budget = 100% - SLO

If SLO = 99.9% availability
Error Budget = 0.1%

Per month (30 days):
Allowed downtime = 30 * 24 * 60 * 0.001 = 43.2 minutes
```

### Alerting Strategies

**Good Alerts**
- Actionable: someone can do something about it
- Urgent: needs immediate attention
- Not noisy: few enough to be meaningful

**Alert on Symptoms, Not Causes**
```
# Bad: Alert on cause
alert: HighCPU
expr: cpu_usage > 90%

# Good: Alert on user-facing symptom
alert: HighLatency
expr: histogram_quantile(0.99, http_request_duration_seconds) > 0.5

# Good: Alert on error rate
alert: HighErrorRate
expr: rate(http_requests_total{status=~"5.."}[5m]) / rate(http_requests_total[5m]) > 0.01
```

**Multi-Window Burn Rate Alerts**
```
# Fast burn — immediate attention
alert: ErrorBudgetFastBurn
expr: (
  rate(errors[1h]) / rate(requests[1h]) > (14.4 * error_budget_consumption_rate)
  and
  rate(errors[5m]) / rate(requests[5m]) > (14.4 * error_budget_consumption_rate)
)

# Slow burn — investigate soon
alert: ErrorBudgetSlowBurn
expr: (
  rate(errors[6h]) / rate(requests[6h]) > (1 * error_budget_consumption_rate)
  and
  rate(errors[30m]) / rate(requests[30m]) > (1 * error_budget_consumption_rate)
)
```

---

## SECURITY PATTERNS

### OWASP Top 10 (2021)

| Rank | Vulnerability | Prevention |
|------|---------------|------------|
| 1 | Broken Access Control | Authorization checks, deny by default, RBAC/ABAC |
| 2 | Cryptographic Failures | TLS everywhere, strong algorithms, proper key management |
| 3 | Injection | Parameterized queries, input validation, encoding |
| 4 | Insecure Design | Threat modeling, security requirements, secure patterns |
| 5 | Security Misconfiguration | Hardened defaults, minimal features, automated verification |
| 6 | Vulnerable Components | Keep dependencies updated, monitor for vulnerabilities |
| 7 | Auth Failures | MFA, strong passwords, session management, rate limiting |
| 8 | Integrity Failures | Digital signatures, trusted sources, CI/CD security |
| 9 | Logging Failures | Log security events, protect logs, monitor for breaches |
| 10 | SSRF | Validate URLs, allowlist destinations, deny by default |

### Secure Coding Practices

**Input Validation**
```python
import re
from pydantic import BaseModel, validator, EmailStr

class UserInput(BaseModel):
    username: str
    email: EmailStr
    age: int

    @validator('username')
    def validate_username(cls, v):
        if not re.match(r'^[a-zA-Z0-9_]{3,30}$', v):
            raise ValueError('Invalid username format')
        return v

    @validator('age')
    def validate_age(cls, v):
        if not 0 <= v <= 150:
            raise ValueError('Age must be between 0 and 150')
        return v

# Usage — fails on invalid input
try:
    user = UserInput(username="valid_user", email="user@example.com", age=25)
except ValidationError as e:
    # Handle validation error
    pass
```

**SQL Injection Prevention**
```python
# NEVER do this
query = f"SELECT * FROM users WHERE id = {user_id}"  # VULNERABLE

# Always use parameterized queries
cursor.execute("SELECT * FROM users WHERE id = %s", (user_id,))

# With ORM (SQLAlchemy)
user = session.query(User).filter(User.id == user_id).first()
```

**Output Encoding**
```python
from markupsafe import escape

# XSS prevention — encode output
user_input = "<script>alert('xss')</script>"
safe_output = escape(user_input)  # &lt;script&gt;alert('xss')&lt;/script&gt;

# In templates (Jinja2) — auto-escaped by default
# {{ user_input }}  <- Safe

# For JSON APIs
import json
response = json.dumps({"message": user_input})  # Automatically escaped
```

### Authentication Patterns

**JWT (JSON Web Token)**
```python
import jwt
from datetime import datetime, timedelta

SECRET_KEY = "your-secret-key"  # Store securely!

def create_token(user_id: str, roles: list) -> str:
    payload = {
        "sub": user_id,
        "roles": roles,
        "iat": datetime.utcnow(),
        "exp": datetime.utcnow() + timedelta(hours=1)
    }
    return jwt.encode(payload, SECRET_KEY, algorithm="HS256")

def verify_token(token: str) -> dict:
    try:
        payload = jwt.decode(token, SECRET_KEY, algorithms=["HS256"])
        return payload
    except jwt.ExpiredSignatureError:
        raise AuthenticationError("Token expired")
    except jwt.InvalidTokenError:
        raise AuthenticationError("Invalid token")
```

**OAuth 2.0 Flows**

| Flow | Use Case |
|------|----------|
| Authorization Code | Web apps with backend |
| Authorization Code + PKCE | Mobile/SPA apps |
| Client Credentials | Machine-to-machine |
| Device Code | Limited-input devices (TV, CLI) |

**Password Storage**
```python
import bcrypt

def hash_password(password: str) -> bytes:
    salt = bcrypt.gensalt(rounds=12)  # Work factor
    return bcrypt.hashpw(password.encode(), salt)

def verify_password(password: str, hashed: bytes) -> bool:
    return bcrypt.checkpw(password.encode(), hashed)
```

### Authorization Patterns

**RBAC (Role-Based Access Control)**
```python
class Permission(Enum):
    READ = "read"
    WRITE = "write"
    DELETE = "delete"
    ADMIN = "admin"

ROLES = {
    "viewer": [Permission.READ],
    "editor": [Permission.READ, Permission.WRITE],
    "admin": [Permission.READ, Permission.WRITE, Permission.DELETE, Permission.ADMIN]
}

def has_permission(user_roles: list, required: Permission) -> bool:
    user_permissions = set()
    for role in user_roles:
        user_permissions.update(ROLES.get(role, []))
    return required in user_permissions

# Usage
@require_permission(Permission.WRITE)
def update_document(doc_id, content):
    pass
```

**ABAC (Attribute-Based Access Control)**
```python
from dataclasses import dataclass

@dataclass
class PolicyContext:
    user: User
    resource: Resource
    action: str
    environment: dict

class Policy:
    def evaluate(self, context: PolicyContext) -> bool:
        raise NotImplementedError

class DocumentOwnerPolicy(Policy):
    def evaluate(self, context: PolicyContext) -> bool:
        return context.resource.owner_id == context.user.id

class WorkingHoursPolicy(Policy):
    def evaluate(self, context: PolicyContext) -> bool:
        hour = context.environment.get("current_hour", 0)
        return 9 <= hour <= 17

class PolicyEngine:
    def __init__(self, policies: list[Policy]):
        self.policies = policies

    def authorize(self, context: PolicyContext) -> bool:
        return all(policy.evaluate(context) for policy in self.policies)
```

### Secrets Management

**Never Hardcode Secrets**
```python
# NEVER do this
API_KEY = "sk-1234567890abcdef"

# Use environment variables
import os
API_KEY = os.environ.get("API_KEY")

# Or use secrets manager
from aws_secretsmanager import get_secret
API_KEY = get_secret("my-api-key")
```

**Secrets Management Best Practices**
1. Store secrets in dedicated secrets manager (Vault, AWS Secrets Manager)
2. Rotate secrets regularly
3. Use short-lived credentials when possible
4. Audit secret access
5. Different secrets per environment
6. Never log secrets

### Encryption

**Encryption at Rest**
```python
from cryptography.fernet import Fernet

# Generate key (store securely!)
key = Fernet.generate_key()
cipher = Fernet(key)

# Encrypt
plaintext = b"sensitive data"
ciphertext = cipher.encrypt(plaintext)

# Decrypt
decrypted = cipher.decrypt(ciphertext)
```

**Encryption in Transit**
- Always use TLS 1.2 or higher
- Proper certificate validation
- HSTS (HTTP Strict Transport Security)

**Security Headers**
```python
# FastAPI example
from fastapi import FastAPI
from starlette.middleware import Middleware
from starlette.middleware.httpsredirect import HTTPSRedirectMiddleware

app = FastAPI()

@app.middleware("http")
async def add_security_headers(request, call_next):
    response = await call_next(request)
    response.headers["X-Content-Type-Options"] = "nosniff"
    response.headers["X-Frame-Options"] = "DENY"
    response.headers["X-XSS-Protection"] = "1; mode=block"
    response.headers["Strict-Transport-Security"] = "max-age=31536000; includeSubDomains"
    response.headers["Content-Security-Policy"] = "default-src 'self'"
    return response
```

---

## API DESIGN

### REST Principles

**Resource-Oriented Design**
```
# Resources are nouns, not verbs
GET    /users           # List users
POST   /users           # Create user
GET    /users/123       # Get user
PUT    /users/123       # Replace user
PATCH  /users/123       # Update user
DELETE /users/123       # Delete user

# Nested resources for relationships
GET    /users/123/orders         # User's orders
POST   /users/123/orders         # Create order for user
GET    /users/123/orders/456     # Specific order

# Don't use verbs in URLs
# Bad:  POST /users/123/activate
# Good: PATCH /users/123 {"status": "active"}
```

**HTTP Status Codes**

| Code | Meaning | Use When |
|------|---------|----------|
| 200 | OK | Successful GET, PUT, PATCH |
| 201 | Created | Successful POST creating resource |
| 204 | No Content | Successful DELETE |
| 400 | Bad Request | Invalid input |
| 401 | Unauthorized | Authentication required |
| 403 | Forbidden | Authenticated but not allowed |
| 404 | Not Found | Resource doesn't exist |
| 409 | Conflict | Resource state conflict |
| 422 | Unprocessable Entity | Validation failed |
| 429 | Too Many Requests | Rate limited |
| 500 | Internal Server Error | Server error |

**Richardson Maturity Model**

| Level | Description |
|-------|-------------|
| 0 | Single URI, single HTTP verb (RPC over HTTP) |
| 1 | Multiple URIs (resources), single verb |
| 2 | Multiple URIs + HTTP verbs (GET, POST, PUT, DELETE) |
| 3 | HATEOAS — Hypermedia links for discoverability |

### API Versioning

**URL Versioning**
```
GET /v1/users
GET /v2/users
```
Pros: Explicit, easy to understand
Cons: Changes URL, can break caching

**Header Versioning**
```
GET /users
Accept: application/vnd.myapi.v2+json
```
Pros: Clean URLs
Cons: Less visible, harder to test

**Query Parameter**
```
GET /users?version=2
```
Pros: Simple to use
Cons: Mixes versioning with query params

**Recommendation**: URL versioning for major versions, backward-compatible changes within versions

### Pagination

**Offset-Based**
```
GET /users?offset=20&limit=10

Response:
{
  "data": [...],
  "pagination": {
    "offset": 20,
    "limit": 10,
    "total": 150
  }
}
```
Pros: Simple, allows jumping to page
Cons: Inconsistent results if data changes, slow for large offsets

**Cursor-Based**
```
GET /users?cursor=eyJpZCI6MTAwfQ&limit=10

Response:
{
  "data": [...],
  "pagination": {
    "next_cursor": "eyJpZCI6MTEwfQ",
    "has_more": true
  }
}
```
Pros: Consistent results, efficient for large datasets
Cons: Can't jump to arbitrary page

### Error Handling

**RFC 7807 Problem Details**
```json
{
  "type": "https://api.example.com/errors/validation",
  "title": "Validation Error",
  "status": 422,
  "detail": "One or more fields failed validation",
  "instance": "/users/123",
  "errors": [
    {
      "field": "email",
      "message": "Invalid email format"
    },
    {
      "field": "age",
      "message": "Must be a positive integer"
    }
  ]
}
```

**Error Response Implementation**
```python
from fastapi import HTTPException
from pydantic import BaseModel

class ErrorDetail(BaseModel):
    type: str
    title: str
    status: int
    detail: str
    instance: str = None
    errors: list = None

@app.exception_handler(ValidationError)
async def validation_exception_handler(request, exc):
    return JSONResponse(
        status_code=422,
        content=ErrorDetail(
            type="https://api.example.com/errors/validation",
            title="Validation Error",
            status=422,
            detail="Request validation failed",
            instance=str(request.url),
            errors=[{"field": e["loc"][-1], "message": e["msg"]} for e in exc.errors()]
        ).dict()
    )
```

### Rate Limiting

**Token Bucket Algorithm**
```python
import time
from collections import defaultdict

class RateLimiter:
    def __init__(self, rate: int, per: int):
        self.rate = rate  # tokens per period
        self.per = per    # period in seconds
        self.buckets = defaultdict(lambda: {"tokens": rate, "last": time.time()})

    def is_allowed(self, key: str) -> bool:
        bucket = self.buckets[key]
        now = time.time()

        # Refill tokens based on elapsed time
        elapsed = now - bucket["last"]
        bucket["tokens"] = min(self.rate, bucket["tokens"] + elapsed * (self.rate / self.per))
        bucket["last"] = now

        if bucket["tokens"] >= 1:
            bucket["tokens"] -= 1
            return True
        return False

# Usage: 100 requests per minute
limiter = RateLimiter(rate=100, per=60)

@app.middleware("http")
async def rate_limit_middleware(request, call_next):
    client_ip = request.client.host
    if not limiter.is_allowed(client_ip):
        return JSONResponse(
            status_code=429,
            content={"error": "Too many requests"},
            headers={"Retry-After": "60"}
        )
    return await call_next(request)
```

### GraphQL Trade-offs

**When to Use GraphQL**
- Multiple clients with different data needs
- Complex, nested data requirements
- Reducing over-fetching and under-fetching
- API used by frontend teams you control

**When to Use REST**
- Simple CRUD operations
- File uploads/downloads
- Caching is important
- Public API with many consumers
- Team more experienced with REST

**N+1 Problem Solution (DataLoader)**
```python
from aiodataloader import DataLoader

async def batch_load_users(user_ids):
    users = await db.query("SELECT * FROM users WHERE id IN %s", user_ids)
    user_map = {u.id: u for u in users}
    return [user_map.get(id) for id in user_ids]

user_loader = DataLoader(batch_load_users)

# In resolver
async def resolve_author(post, info):
    return await user_loader.load(post.author_id)
```

### API Documentation (OpenAPI)

```yaml
openapi: 3.0.3
info:
  title: User API
  version: 1.0.0
  description: API for managing users

paths:
  /users:
    get:
      summary: List users
      parameters:
        - name: limit
          in: query
          schema:
            type: integer
            default: 20
      responses:
        '200':
          description: Successful response
          content:
            application/json:
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/User'
    post:
      summary: Create user
      requestBody:
        required: true
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/CreateUser'
      responses:
        '201':
          description: User created

components:
  schemas:
    User:
      type: object
      properties:
        id:
          type: string
        email:
          type: string
          format: email
        name:
          type: string
```

### Backward Compatibility

**Safe Changes (Non-Breaking)**
- Adding new endpoints
- Adding optional request fields
- Adding response fields
- Adding new enum values (if client ignores unknown)

**Breaking Changes (Require Version Bump)**
- Removing endpoints
- Removing/renaming fields
- Changing field types
- Adding required fields
- Changing URL structure

**Deprecation Strategy**
```python
@app.get("/users/{user_id}")
async def get_user(user_id: str, response: Response):
    # Add deprecation headers
    response.headers["Deprecation"] = "true"
    response.headers["Sunset"] = "Sat, 01 Jan 2025 00:00:00 GMT"
    response.headers["Link"] = '</v2/users/{user_id}>; rel="successor-version"'

    return user
```

---

## QUICK CHECKLISTS (EXPANDED)

### For DDD Implementation
- [ ] Is ubiquitous language used consistently?
- [ ] Are bounded contexts clearly defined?
- [ ] Is there an anti-corruption layer for legacy systems?
- [ ] Are aggregates kept small?
- [ ] Are references between aggregates by ID only?
- [ ] Is eventual consistency handled between aggregates?

### For Microservices
- [ ] Is each service independently deployable?
- [ ] Does each service have its own database?
- [ ] Are services communicating via APIs (not shared database)?
- [ ] Is there a circuit breaker for external calls?
- [ ] Is service discovery in place?
- [ ] Are sagas used for distributed transactions?

### For Observability
- [ ] Are logs structured (JSON)?
- [ ] Are correlation IDs propagated?
- [ ] Are traces exported to collector?
- [ ] Are SLIs/SLOs defined?
- [ ] Are alerts on symptoms (not causes)?
- [ ] Is there a runbook for each alert?

### For Security
- [ ] Is input validated and sanitized?
- [ ] Are queries parameterized (no SQL injection)?
- [ ] Are secrets stored securely (not hardcoded)?
- [ ] Is authentication/authorization in place?
- [ ] Is data encrypted at rest and in transit?
- [ ] Are security headers set?
- [ ] Are dependencies scanned for vulnerabilities?

### For API Design
- [ ] Are resources properly named (nouns, not verbs)?
- [ ] Are HTTP methods used correctly?
- [ ] Are status codes appropriate?
- [ ] Is pagination implemented?
- [ ] Is rate limiting in place?
- [ ] Is versioning strategy defined?
- [ ] Is error format consistent (RFC 7807)?
- [ ] Is API documented (OpenAPI)?

---

*"Any fool can write code that a computer can understand. Good programmers write code that humans can understand."* — Martin Fowler

*"The best code is no code at all."* — Jeff Atwood

*"Premature optimization is the root of all evil."* — Donald Knuth

*"Make it work, make it right, make it fast."* — Kent Beck

*"Programs must be written for people to read, and only incidentally for machines to execute."* — Abelson & Sussman

*"Simplicity is prerequisite for reliability."* — Edsger Dijkstra

*"It is not enough for code to work."* — Robert C. Martin
