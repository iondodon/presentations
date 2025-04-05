---
title: "**Clean Code**"
sub_title: by Robert C. Martin (Summarized)
---

Chapter 1 — The Foundation of Professional Software
===

<!-- 
speaker_note: |
  Welcome to Chapter 1. This is where we set the stage for everything to come.
  Clean Code isn’t just about writing something that works — it’s about writing code that lasts.
  Let’s dig into what makes clean code such a core part of being a professional.
-->

<!-- end_slide -->

Why Clean Code?
===

- Code is read far more often than it's written.
- Clean code reduces bugs, improves team velocity, and builds trust.
- Writing clean code is a sign of professionalism.

<!-- 
speaker_note: |
  Let’s face it — we spend more time reading code than writing it.
  And bad code slows us down, introduces bugs, and frustrates everyone involved.
  Writing clean code isn’t optional if you want to call yourself a professional.
-->

<!-- end_slide -->

There Will Be Code
===

- Some believe code will disappear — replaced by specs or visual tools.
- But code *is* the specification — it's how we express exact behavior.
- Higher abstraction doesn't remove code — it transforms it.

<!-- 
speaker_note: |
  You might hear people say, “Soon we won’t need to write code.”
  But the truth is: code is how we capture detail. It *is* the final layer of specification.
  Even with AI or high-level tools, someone will always need to define the logic precisely — and that’s code.
-->

<!-- end_slide -->

Why Bad Code Happens
===

- We often trade quality for speed — under pressure.
- Common excuses: tight deadlines, fatigue, "we'll fix it later."
- Reality: later almost always means *never*.

<!-- 
speaker_note: |
  Let’s be honest — we’ve all made a mess to get something working.
  Deadlines, stress, or that "I’ll clean it up later" mindset creep in.
  But as LeBlanc’s Law says: “Later equals never.” Those messes stay with us.
-->

<!-- end_slide -->

The Cost of Messy Code
===

- Short-term gains, long-term pain.
- Messy code leads to:
  - Fragile systems
  - Slow development
  - Frustrated teams

<!-- 
speaker_note: |
  Messy code builds technical debt fast.
  What started as a small trade-off turns into a mountain of pain — where every change breaks three other things.
  Over time, your team slows to a crawl. Morale drops. Delivery suffers.
-->

<!-- end_slide -->

The Grand Redesign in the Sky
===

- Eventually, teams beg for a rewrite.
- A "tiger team" builds Version 2.0.
- But without changing habits, the new system becomes just as bad.

<!-- 
speaker_note: |
  I've seen this pattern too many times.
  The team can’t take it anymore, so they start from scratch. But they bring the same bad habits.
  Six months in, the new codebase looks just as bad.
  Rewrites don’t solve bad discipline — they repeat it.
-->

<!-- end_slide -->

Attitude Makes the Difference
===

- Clean code is a matter of attitude, not just skill.
- Our job is to advocate for quality — even under pressure.
- Push back professionally when speed threatens sustainability.

<!-- 
speaker_note: |
  This is key: writing clean code is a mindset.
  It's about pride in your work, responsibility to your team, and the courage to defend quality — even when it’s hard.
  That’s what separates professionals from amateurs.
-->

<!-- end_slide -->

What Is Clean Code?
===

- Code that is easy to read and understand.
- Clear, expressive, and intention-revealing.
- Like a good story — every line should make sense.

<!-- 
speaker_note: |
  Clean code doesn’t hide meaning — it reveals it.
  It reads like prose. Someone new to the team should be able to follow along without needing a translator.
  That’s the level of clarity we’re aiming for.
-->

<!-- end_slide -->

The Boy Scout Rule
===

> "Always leave the campground cleaner than you found it."

- Improve code every time you touch it.
- Small refactors = big long-term impact.

<!-- 
speaker_note: |
  This principle is gold.
  Don’t wait for a big refactor. If you're in the code anyway, make it a bit better than you found it.
  Rename a variable. Break a method. These small acts compound over time.
-->

<!-- end_slide -->

Conclusion
===

- Clean code is a mindset — and a practice.
- It takes discipline, patience, and pride.
- Up next: the first tool in your clean code toolbox — **meaningful names**.

<!-- 
speaker_note: |
  So that's Chapter 1 — a powerful reminder that clean code isn’t just about style, it’s about responsibility.
  Next, we’ll dive into one of the most powerful tools you have for clarity: choosing great names.
-->

<!-- end_slide -->

Chapter 2 — Meaningful Names
===

<!-- 
speaker_note: |
  Welcome to Chapter 2 — probably the most underestimated chapter in the whole book.
  Naming things well is one of the simplest ways to write clean, readable code — and yet so often, we rush it.
  Let’s fix that.
-->

<!-- end_slide -->

Why Names Matter
===

- Code is read 10x more than it's written.
- Good names eliminate the need for comments.
- They reduce bugs and improve collaboration.

<!-- 
speaker_note: |
  We spend most of our time reading code, not writing it.
  Names are our first, best chance to explain what the code is doing — so why waste that chance?
-->

<!-- end_slide -->

Reveal Intent
===

- Choose names that answer: *What is this? What does it do?*
- ❌ `d` or `tmp`
- ✅ `elapsedTimeInDays`, `totalRevenue`

<!-- 
speaker_note: |
  A name should eliminate confusion, not cause it.
  If you have to explain it in a comment, you probably need a better name instead.
  Let the name do the talking.
-->

<!-- end_slide -->

Avoid Disinformation
===

- Misleading names cause subtle bugs.
- ❌ `accountList` when it's a `Set`
- ❌ `timeout` (in ms) → name it `timeoutInMillis`

<!-- 
speaker_note: |
  Think of names as contracts. If the name says one thing and the reality is another, it’s a broken contract.
  Keep names honest — even the little ones.
-->

<!-- end_slide -->

Make Meaningful Distinctions
===

- Don’t use noise words or numbers.
- ❌ `info1`, `info2`, `userDataTmp`
- ✅ `userProfile`, `adminProfile`

<!-- 
speaker_note: |
  Think of names like labels. If you can’t tell two variables apart by name, something’s wrong.
  Give each item a name that reflects its *role*, not its *order*.
-->

<!-- end_slide -->

Use Pronounceable & Searchable Names
===

- Pronounceable: ✅ `customerAddress`, ❌ `custAddr`
- Searchable: ✅ `elapsedTime`, ❌ `k`

<!-- 
speaker_note: |
  If a name is hard to say, people won’t say it. If it’s hard to search, you’ll hate maintaining it.
  Give your future self and your teammates a break — use clear, searchable names.
-->

<!-- end_slide -->

Avoid Encodings and Prefixes
===

- ❌ `strName`, `iCount`, `bDone`
- ✅ `name`, `count`, `isFinished`
- Let tools handle type — focus names on purpose.

<!-- 
speaker_note: |
  Encoding types in names made sense in the ‘90s. Today, it’s just noise.
  Your IDE already knows the type. Focus the name on what it *means*.
-->

<!-- end_slide -->

Consistent Vocabulary
===

- Use one word per concept.
- ❌ `fetch`, `retrieve`, `get` used interchangeably
- ✅ Choose one — and stick to it.

<!-- 
speaker_note: |
  This is about consistency. If `get` means something in your codebase, use it everywhere for that concept.
  Don't make your readers guess whether `fetch`, `retrieve`, and `get` do the same thing.
-->

<!-- end_slide -->

Provide Context — When Needed
===

- ✅ `addressState` instead of `state`
- ❌ `productId` inside a `Product` class → just `id` is fine

<!-- 
speaker_note: |
  Use context to disambiguate, but don’t go overboard.
  If you’re inside a `Product` class, you don’t need to call everything `productSomething`.
-->

<!-- end_slide -->

Conclusion
===

- Naming is a communication skill, not just a technical one.
- Good names reduce confusion, bugs, and wasted time.
- Great code starts with great names.

<!-- 
speaker_note: |
  Naming is where clean code begins. Take the time to name things well, and you’ll save hours of debugging and explaining later.
  Up next — functions: how to write them clean, clear, and powerful.
-->

<!-- end_slide -->

Chapter 3 — Functions
===

<!-- 
speaker_note: |
  This chapter is the heart of Clean Code. If you can write good functions, everything else becomes easier.
  Functions are where logic lives — and they can either make a codebase joyful or painful to work in.
  Let’s break down what makes a great function.
-->

<!-- end_slide -->

Functions Should Be Small
===

- The first rule: **small**. The second rule: **smaller than that**.
- Ideally: 1–5 lines.
- Each function should do one thing — and do it well.

```java
// ❌ Too large
public void processUserInput(String input) {
    if (input != null && input.length() > 0) {
        String[] parts = input.split(",");
        for (String part : parts) {
            if (!part.isEmpty()) {
                saveToDatabase(part);
            }
        }
    }
}

// ✅ Split into small, clear steps
public void processUserInput(String input) {
    if (isValid(input)) {
        for (String part : parse(input)) {
            save(part);
        }
    }
}
```

<!-- 
speaker_note: |
  Small functions are easier to test, easier to read, and easier to reuse.
  The second version shows how we can name the steps, making the logic clear — even if we don't see the details of each helper method.
-->

<!-- end_slide -->

Do One Thing
===

- Every function should do exactly **one thing**.
- If it does more than one thing — extract the second thing into its own function.
- "One thing" means one **responsibility**, not one line of code.

```java
// ❌ Does multiple things
public void saveUserData(User user) {
    validate(user);
    log(user);
    repository.save(user);
}

// ✅ Do one thing each
public void saveUserData(User user) {
    validate(user);
    save(user);
}
```

<!-- 
speaker_note: |
  The idea of "one thing" is about conceptual integrity.
  If your function validates, logs, and saves — it’s doing at least three things.
  Extracting those steps improves testability and reuse.
-->

<!-- end_slide -->

Use Descriptive Names
===

- Name functions for **what they do**, not how they do it.
- Prefer verbs: `calculateTotal()`, `renderReport()`, `validateInput()`
- Avoid vague names: `handle()`, `process()`, `manage()`

```java
// ❌ Vague
handle(customer);

// ✅ Clear
sendInvoiceTo(customer);
```

<!-- 
speaker_note: |
  If your function name is ambiguous, the reader has to dig into the body to understand it.
  Let the name do the heavy lifting — it should describe the intention, not the mechanics.
-->

<!-- end_slide -->

Function Arguments
===

- Fewer is better:
  - ✅ 0–2 is ideal
  - ⚠️ 3 is questionable
  - 🚫 4+ is a code smell
- Use objects instead of multiple primitive arguments.

```java
// ❌ Too many primitives
scheduleMeeting("Team Sync", 30, "Zoom", true);

// ✅ Use a parameter object
scheduleMeeting(new Meeting("Team Sync", 30, "Zoom", true));
```

<!-- 
speaker_note: |
  Arguments make functions harder to understand and test.
  Wrapping multiple related arguments into an object gives them meaning and reduces cognitive load.
-->

<!-- end_slide -->

Avoid Output Arguments
===

- Prefer return values over modifying passed-in parameters.
- Output arguments hide side effects and make testing harder.

```java
// ❌ Modifies the argument
void fillList(List<String> list) {
    list.add("item1");
    list.add("item2");
}

// ✅ Returns the result
List<String> getList() {
    return List.of("item1", "item2");
}
```

<!-- 
speaker_note: |
  Output arguments break the principle of least surprise.
  Instead of asking the function to fill something, just let it return a result. That makes data flow explicit.
-->

<!-- end_slide -->

No Side Effects
===

- A function should do what it says — and **only** what it says.
- Side effects create hidden complexity and bugs.

```java
// ❌ Implicit side effect: caching
public String getUser(String id) {
    if (!cache.contains(id)) {
        cache.put(id, db.fetch(id));
    }
    return cache.get(id);
}

// ✅ Separate the concerns
public String getUser(String id) {
    return db.fetch(id);
}
```

<!-- 
speaker_note: |
  Side effects are things the function does that the name doesn't suggest.
  Caching, logging, saving — these should be isolated. Don’t surprise your callers.
-->

<!-- end_slide -->

Use Exceptions, Not Error Codes
===

- Return codes require condition checking everywhere.
- Exceptions separate error-handling logic from main logic.

```java
// ❌ Error code
if (deleteUser(user) == ERROR_NOT_FOUND) {
    // handle error
}

// ✅ Exception
try {
    deleteUser(user);
} catch (UserNotFoundException e) {
    // handle error
}
```

<!-- 
speaker_note: |
  Error codes pollute your main logic with repetitive checking.
  Exceptions let you focus on the happy path and handle errors when needed.
-->

<!-- end_slide -->

Functions Should Read Top-Down
===

- Call high-level functions first, then details below.
- Let the function tell a **story** from beginning to end.

```java
public void processOrder(Order order) {
    validate(order);
    calculateTotals(order);
    charge(order);
    sendConfirmation(order);
}
```

<!-- 
speaker_note: |
  Reading a function should feel like reading a paragraph — clear, logical, and linear.
  Details can be broken into well-named helpers, shown below the high-level narrative.
-->

<!-- end_slide -->

DRY and Reuse Helpers
===

- Don’t repeat logic — extract shared steps.
- Even small, obvious logic can be extracted for clarity.

```java
// ❌ Repeated parsing
if (value.trim().equals("")) ...
if (value.trim().length() < 3) ...

// ✅ Helper method
if (isEmpty(value)) ...
```

<!-- 
speaker_note: |
  Don’t copy-paste the same logic in multiple places.
  Extract and name it — even if it's just trimming and checking length.
  That makes it easier to update later and improves readability now.
-->

<!-- end_slide -->

Conclusion
===

- Functions are the **core building blocks** of clean code.
- Keep them **small**, **focused**, and **descriptive**.
- Minimize arguments, avoid side effects, and write for readability.

<!-- 
speaker_note: |
  Clean functions = clean code.
  The principles here — small size, clear naming, one responsibility — have a ripple effect across your codebase.
  Next up: how to write meaningful comments — when you actually need them.
-->
<!-- end_slide -->

Chapter 4 — Comments
===

<!-- 
speaker_note: |
  Chapter 4 is about comments — when they help, when they hurt, and why less is usually more.
  Uncle Bob isn’t anti-comment. He’s just pro-clarity. And often, comments are a sign that the code itself isn’t clear.
-->

<!-- end_slide -->

The Purpose of Comments
===

- Comments should **compensate for failure to express intent in code**.
- They are **not a substitute** for clear naming or structure.
- Good comments explain *why*, not *what*.

<!-- 
speaker_note: |
  Think of comments as a bandage — not a cure.
  If your code isn’t self-explanatory, a comment can help — but fixing the code is better.
  Use comments when intent would be otherwise unclear, not to explain poor naming or long methods.
-->

<!-- end_slide -->

Explain Why, Not What
===

- ❌ Don’t explain obvious code:
```java
// increment i by 1
i++;
```

- ✅ Do explain *why* something is done:
```java
// Compensate for timezone offset
adjustedTime = rawTime + offset;
```

<!-- 
speaker_note: |
  A comment that says "increment i by 1" is just noise.
  But explaining the business reason for a calculation? That’s useful context.
  Help readers understand the reasoning, not the mechanics.
-->

<!-- end_slide -->

Clarify Intent When Code Can’t
===

- Use comments to document decisions that code alone can’t express:
  - Regulatory requirements
  - Performance hacks
  - Workarounds for known bugs or issues

```java
// Required by EU regulation: must log all failed login attempts
logFailure(user);
```

<!-- 
speaker_note: |
  Sometimes your code is doing something that seems odd — but it’s necessary.
  In those cases, a quick comment explaining the reason can prevent someone from "cleaning it up" later and breaking a requirement.
-->

<!-- end_slide -->

Avoid Redundant Comments
===

- ❌ Redundant:
```java
// Set name to "John"
user.setName("John");
```

- ✅ Better: make the method name self-explanatory:
```java
user.setDefaultName();
```

<!-- 
speaker_note: |
  Redundant comments waste time and space. If your method or variable names are good, the comment shouldn’t be necessary.
  In this case, the solution is better naming — not better commenting.
-->

<!-- end_slide -->

Avoid Commented-Out Code
===

- ❌ Don’t leave dead code in comments:
```java
// old implementation
// user.save(false);
```

- ✅ Use version control to track history.

<!-- 
speaker_note: |
  Commented-out code adds clutter and confusion.
  That’s what version control is for. If you need to restore something, use Git — not comment blocks.
-->

<!-- end_slide -->

Use Legal and Informative Comments
===

- ✅ Legal/attribution comments (if required)
- ✅ TODOs — when tracked and actionable
- ✅ Explanatory comments for business rules, hacks, or gotchas

```java
// TODO: Remove this when legacy API is deprecated
```

<!-- 
speaker_note: |
  Not all comments are bad. Legal headers, TODOs, and necessary clarifications are fine.
  Just make sure they’re actually helpful — and kept up to date.
-->

<!-- end_slide -->

Use Javadoc — But Wisely
===

- ✅ Use Javadoc for public APIs
- ❌ Don’t use it to explain obvious things
- Keep it current — outdated Javadoc is worse than none

```java
/**
 * Calculates tax for a given invoice.
 * @param invoice the invoice to tax
 * @return total tax owed
 */
```

<!-- 
speaker_note: |
  Javadoc is helpful — especially for public interfaces. But keep it concise and current.
  Outdated documentation misleads users and developers alike.
-->

<!-- end_slide -->

Conclusion
===

- Comments are a fallback — not a first choice.
- Clean code speaks for itself.
- Use comments to add value — not to excuse unclear code.

<!-- 
speaker_note: |
  A good developer minimizes the need for comments by writing expressive code.
  But when comments are needed, use them with purpose — to share reasoning, requirements, or important caveats.
  In the next chapter, we’ll look at formatting: how the structure of code affects its readability.
-->

<!-- end_slide -->

Chapter 5 — Formatting
===

<!-- 
speaker_note: |
  Welcome to Chapter 5. Now that we’ve covered functions and comments, let’s talk about the shape of your code.
  Formatting isn’t about style guides — it’s about communication. The way code is laid out should help readers understand it at a glance.
-->

<!-- end_slide -->

The Purpose of Formatting
===

- Formatting creates visual structure.
- It helps readers:
  - Understand flow
  - See relationships between code blocks
  - Scan for relevant logic quickly
- Consistent formatting means fewer distractions.

<!-- 
speaker_note: |
  Formatting gives your code rhythm and structure.
  Think of it like typesetting in a book — good formatting makes reading smooth, bad formatting makes it exhausting.
-->

<!-- end_slide -->

Vertical Formatting — Top to Bottom
===

- Readers read code **top to bottom**.
- Code should be ordered:
  1. High-level concepts first
  2. Details and helpers below
- Related code should be close together.

```java
public class ReportGenerator {
    public void generate() {
        fetchData();
        formatData();
        exportData();
    }

    // helper methods
    private void fetchData() {...}
    private void formatData() {...}
    private void exportData() {...}
}
```

<!-- 
speaker_note: |
  Make your code flow like a story. Start with what matters most — then move into details.
  If related code is scattered, it makes comprehension harder.
-->

<!-- end_slide -->

Vertical Openness
===

- Use vertical space to separate distinct concepts.
- Don’t cram multiple methods or blocks together.
- Group lines that belong together, and separate unrelated ones.

```java
// Good vertical spacing
validateInput(input);

calculateResults(input);

saveResults(results);
```

<!-- 
speaker_note: |
  Vertical openness is about giving the reader breathing room.
  Too little spacing feels dense. Too much and you lose context. Strike a visual rhythm.
-->

<!-- end_slide -->

Horizontal Formatting — Line Structure
===

- Lines should be short: ~80–120 characters max.
- Break long statements into multiple lines.
- Align parameters and chained method calls for clarity.

```java
// Better formatting for clarity
Order order = new Order(
    customerId,
    itemList,
    shippingAddress,
    LocalDate.now()
);
```

<!-- 
speaker_note: |
  Readers scan left to right. If your line runs off the screen, they lose context.
  Break things up so the eye can rest and the brain can follow.
-->

<!-- end_slide -->

Indentation and Nesting
===

- Each level of nesting = more mental overhead.
- Avoid deeply nested structures.
- Extract blocks into functions when nesting gets deep.

```java
// Refactor deeply nested logic
if (user != null) {
    if (user.isActive()) {
        if (!user.isLocked()) {
            grantAccess(user);
        }
    }
}
```

<!-- 
speaker_note: |
  Deep nesting makes code harder to reason about.
  Flatten your structure by returning early or moving logic into smaller, single-purpose functions.
-->

<!-- end_slide -->

Team Conventions Matter
===

- Pick a consistent style — and stick with it.
- Formatting differences should never be a source of conflict.
- Use automated tools like `prettier`, `eslint`, or IDE settings to enforce standards.

<!-- 
speaker_note: |
  The best formatting style is the one everyone agrees on and applies consistently.
  Don’t waste time debating spaces vs. tabs — automate it and focus on substance.
-->

<!-- end_slide -->

Conclusion
===

- Formatting is about **readability**, not personal taste.
- Well-formatted code reads like well-written prose.
- Respect the reader: structure your code so it tells a story.

<!-- 
speaker_note: |
  Formatting is your first impression. It tells your teammates whether your code is thoughtful or careless.
  Write for humans first — the compiler already understands it.
  In the next chapter, we’ll tackle objects and data structures — and how to use them cleanly.
-->

<!-- end_slide -->

Chapter 6 — Objects and Data Structures
===

<!-- 
speaker_note: |
  Chapter 6 explores the balance between objects and data structures.
  Uncle Bob draws a clear distinction between these two and explains how each should be used — and what not to mix between them.
-->

<!-- end_slide -->

The Difference Between Objects and Data Structures
===

- **Objects** hide data and expose behavior.
- **Data structures** expose data and have no meaningful behavior.

```java
// Object-style
public class User {
    private String name;

    public String getName() {
        return name;
    }

    public void rename(String newName) {
        this.name = newName;
    }
}

// Data structure-style
public class UserData {
    public String name;
}
```

<!-- 
speaker_note: |
  Objects encapsulate — they hide internals and offer controlled access through methods.
  Data structures are transparent — just a bunch of public fields. Both are useful, but in different places.
-->

<!-- end_slide -->

Procedural vs Object-Oriented
===

- Procedural code uses data structures with procedures.
- OO code uses objects that contain both data and behavior.

```java
// Procedural
calculatePay(employee);

// OO
employee.calculatePay();
```

<!-- 
speaker_note: |
  Neither style is wrong, but each serves a purpose.
  OO shines when modeling behaviors. Procedural is better when behaviors apply across many data types.
-->

<!-- end_slide -->

Law of Demeter (Principle of Least Knowledge)
===

- A method should only call:
  - Itself
  - Its own fields
  - Parameters passed in

- Avoid chaining:
```java
// ❌ Violates Law of Demeter
order.getCustomer().getAddress().getPostalCode();

// ✅ Better
PostalCode postalCode = order.getPostalCode();
```

<!-- 
speaker_note: |
  This principle helps prevent tight coupling.
  If you’re constantly reaching into objects inside objects, you’re violating encapsulation.
  Provide methods that do what’s needed directly, instead of making the caller navigate your structure.
-->

<!-- end_slide -->

Data/Object Anti-Symmetry
===

- **Objects**: expose behavior, hide data.
- **Data Structures**: expose data, no behavior.
- Mixing the two leads to maintenance problems.

```java
// ❌ Hybrid (bad)
public class Employee {
    public String name;
    public double salary;

    public void calculatePay() {
        // logic that uses internal state
    }
}

// ✅ Clear separation
public class EmployeeData {
    public String name;
    public double salary;
}

public class PayrollCalculator {
    public double calculatePay(EmployeeData data) {
        // logic here
    }
}
```

<!-- 
speaker_note: |
  Don’t mix paradigms. If you have public fields and behavior together, you’re halfway object, halfway data.
  Decide: are you modeling behavior (object) or raw data (structure)? Keep it clean.
-->

<!-- end_slide -->

Use Data Structures for Data Transfer
===

- DTOs (Data Transfer Objects) are great for:
  - APIs
  - Database models
  - Configuration

- They should have no logic beyond maybe null-checks or defaults.

```java
public class UserDTO {
    public String id;
    public String email;
    public boolean active;
}
```

<!-- 
speaker_note: |
  DTOs are fine — just don’t let them grow behavior.
  Use them to carry data between layers, and keep logic in service or domain classes.
-->

<!-- end_slide -->

Avoid Feature Envy
===

- A function that constantly accesses another object's data probably belongs on that object.

```java
// ❌ Feature envy
public class ReportPrinter {
    public void print(Employee e) {
        System.out.println(e.getName());
        System.out.println(e.getSalary());
    }
}

// ✅ Better: move responsibility
public class Employee {
    public void printReport() {
        System.out.println(name);
        System.out.println(salary);
    }
}
```

<!-- 
speaker_note: |
  If a class spends all its time poking at another class’s fields, it probably doesn’t belong there.
  Let behavior live with the data it needs.
-->

<!-- end_slide -->

Conclusion
===

- Choose **objects** when modeling behavior.
- Use **data structures** for transport and transparency.
- Don’t mix the two — keep designs intentional.

<!-- 
speaker_note: |
  Clean code respects separation of concerns. Objects do things. Data structures hold things.
  Mixing the two leads to fragile code. Be deliberate with your design.
  In the next chapter, we’ll look at error handling — and how to do it without polluting your logic.
-->

<!-- end_slide -->

Chapter 7 — Error Handling
===

<!-- 
speaker_note: |
  Chapter 7 is about writing clean, maintainable error-handling code.
  Uncle Bob emphasizes that error handling is essential — but it shouldn’t make our code messy or unreadable.
-->

<!-- end_slide -->

Use Exceptions Rather Than Return Codes
===

- Exceptions separate error-handling logic from normal code.
- Return codes clutter logic and can be forgotten.

```java
// ❌ Return code style
if (deleteRecord(id) == -1) {
    // handle error
}

// ✅ Exception style
try {
    deleteRecord(id);
} catch (RecordNotFoundException e) {
    // handle error
}
```

<!-- 
speaker_note: |
  Return codes require every caller to check for failure manually — and it’s easy to forget.
  Exceptions make error handling explicit and separate from main logic.
-->

<!-- end_slide -->

Write Your Try-Catch-Finally Statements First
===

- Start with the error handling structure, then fill in the logic.
- Keeps the structure clear and prevents forgotten handling.

```java
try {
    // logic here
} catch (IOException e) {
    logError(e);
} finally {
    cleanUp();
}
```

<!-- 
speaker_note: |
  Writing the structure first helps you think about what can go wrong before diving into the happy path.
  It enforces discipline and reduces error-handling omissions.
-->

<!-- end_slide -->

Use Unchecked Exceptions for Most Errors
===

- Checked exceptions force callers to catch or declare.
- Unchecked exceptions are less intrusive and encourage better design.

```java
public void connect() {
    if (!networkAvailable()) {
        throw new NetworkUnavailableException();
    }
}
```

<!-- 
speaker_note: |
  Uncle Bob argues that checked exceptions often cause more harm than good — they clutter code and break encapsulation.
  Prefer unchecked exceptions unless there’s a strong reason to require handling.
-->

<!-- end_slide -->

Provide Context with Exceptions
===

- Include descriptive messages in exceptions.
- Wrap lower-level exceptions when rethrowing.

```java
throw new StorageException("Could not save file: " + fileName, e);
```

<!-- 
speaker_note: |
  Always include enough context in your exceptions to make debugging easy.
  Don’t just throw a generic error — explain what failed and why.
-->

<!-- end_slide -->

Define Exception Classes for Domain-Specific Problems
===

- Make exceptions meaningful in your application’s language.
- Don’t rely only on generic types.

```java
throw new InvalidOrderException("Order must contain at least one item");
```

<!-- 
speaker_note: |
  Your exceptions should speak the language of your domain.
  Use custom exception classes to make them more readable and easier to manage.
-->

<!-- end_slide -->

Don’t Return Null
===

- Returning `null` forces callers to do null checks.
- It leads to defensive, cluttered code.

```java
// ❌ Bad
public Address getAddress() {
    return null;
}

// ✅ Better
public Optional<Address> getAddress() {
    return Optional.of(address);
}
```

<!-- 
speaker_note: |
  Avoid nulls where possible. They break flow and introduce bugs.
  Use alternatives like `Optional` or throw exceptions when appropriate.
-->

<!-- end_slide -->

Don’t Pass Null
===

- Passing null can cause unexpected failures.
- Require non-null parameters, or validate early.

```java
public void setConfig(Config config) {
    if (config == null) throw new IllegalArgumentException("config must not be null");
    this.config = config;
}
```

<!-- 
speaker_note: |
  Be explicit — make it clear whether a parameter is required.
  Failing fast with a clear exception is better than letting nulls propagate quietly.
-->

<!-- end_slide -->

Conclusion
===

- Handle errors clearly and cleanly.
- Prefer exceptions over return codes.
- Avoid nulls whenever possible.
- Always include enough context in your error messages.

<!-- 
speaker_note: |
  Error handling is part of writing clean code — not something to bolt on afterward.
  Handle errors like you handle logic: clearly, intentionally, and with empathy for whoever will debug it later.
  Next, we’ll explore boundaries — how to keep external systems from polluting your clean codebase.
-->

<!-- end_slide -->

Chapter 8 — Boundaries
===

<!-- 
speaker_note: |
  Chapter 8 is about protecting your code from the instability of external systems — like frameworks, libraries, and tools.
  The core message is: treat boundaries as dangerous terrain. Isolate them.
-->

<!-- end_slide -->

What Are Boundaries?
===

- External systems your code interacts with:
  - Third-party libraries
  - Frameworks (UI, database, network)
  - External APIs
- These things **can and will change**.

<!-- 
speaker_note: |
  Boundaries are where your clean, well-tested code meets the chaos of the outside world.
  It’s where assumptions break, updates happen, and integration pain lives. So we isolate them.
-->

<!-- end_slide -->

Use Adapters to Isolate Third-Party Code
===

- Wrap third-party APIs in your own interfaces.
- Prevent external changes from leaking into your system.

```java
// Third-party class
Map<String, Object> response = externalService.call();

// Wrapped inside your boundary class
public class PaymentGateway {
    public PaymentResponse process() {
        Map<String, Object> data = externalService.call();
        return new PaymentResponse(data);
    }
}
```

<!-- 
speaker_note: |
  If the external API changes, you only have to update your wrapper — not your whole codebase.
  This keeps your domain logic clean and insulated from external churn.
-->

<!-- end_slide -->

Don’t Let Frameworks Drive Your Architecture
===

- Your app should use the framework — not be trapped inside it.
- Keep framework-specific code at the edges.

```java
// ✅ Good: controller delegates to core logic
@RestController
public class OrderController {
    private final OrderService service;

    public ResponseEntity<Order> getOrder(...) {
        return ResponseEntity.ok(service.fetchOrder(...));
    }
}
```

<!-- 
speaker_note: |
  Frameworks are tools, not foundations. Don’t bake them into your core.
  Keep them at the edges, so you can replace or upgrade them without rewriting your whole system.
-->

<!-- end_slide -->

Write Boundary Tests to Explore Behavior
===

- Boundary components are often untrustworthy.
- Use learning tests (a.k.a. characterization tests) to:
  - Explore unknown behavior
  - Lock in expectations

```java
@Test
public void jsonLibraryEncodesDatesCorrectly() {
    String json = encode(new Date(0));
    assertTrue(json.contains("1970"));
}
```

<!-- 
speaker_note: |
  When using a new library or system, write tests to understand how it behaves — especially in edge cases.
  These tests help protect you from silent breaking changes later.
-->

<!-- end_slide -->

Use Dependency Inversion to Decouple Boundaries
===

- High-level code should not depend on low-level details.
- Depend on abstractions.

```java
// ✅ Use interfaces to invert dependencies
public interface EmailService {
    void send(Email email);
}

public class SmtpEmailService implements EmailService {
    public void send(Email email) {
        // SMTP logic here
    }
}
```

<!-- 
speaker_note: |
  Dependency Inversion Principle helps isolate boundaries.
  Your core code should depend on interfaces, not implementations — especially third-party ones.
-->

<!-- end_slide -->

Conclusion
===

- Boundaries are fragile — isolate them.
- Wrap, test, and invert dependencies to keep your code safe.
- Your domain logic should not know or care about the tools at the edges.

<!-- 
speaker_note: |
  Clean code lives at the center — frameworks, tools, and APIs belong at the edges.
  Wrapping and isolating them keeps your architecture clean, flexible, and future-proof.
  Next, we’ll move into unit testing — and how to write tests that are truly clean and maintainable.
-->

<!-- end_slide -->

Chapter 9 — Unit Tests
===

<!-- 
speaker_note: |
  Chapter 9 focuses on writing clean, effective unit tests.
  Uncle Bob argues that clean code isn’t just about production code — it applies just as much to your tests.
-->

<!-- end_slide -->

Clean Tests Are Readable
===

- Tests must be **easy to read** and understand.
- Good tests act as documentation.
- A test should fail loudly and clearly when broken.

```java
@Test
public void shouldReturnZeroForEmptyCart() {
    ShoppingCart cart = new ShoppingCart();
    assertEquals(0, cart.total());
}
```

<!-- 
speaker_note: |
  Tests are your safety net. If they’re hard to understand, they won’t be trusted.
  Make them expressive. Think of tests as executable specifications.
-->

<!-- end_slide -->

Three Laws of TDD
===

1. Don’t write production code unless there's a failing test.
2. Don’t write more of a test than necessary to fail.
3. Don’t write more production code than necessary to pass.

<!-- 
speaker_note: |
  These laws guide Test-Driven Development.
  The cycle is: write a failing test, make it pass, then refactor.
  It keeps you focused and prevents overengineering.
-->

<!-- end_slide -->

Test Structure — The Three A's
===

- **Arrange**: Set up data and dependencies
- **Act**: Execute the code under test
- **Assert**: Check the result

```java
@Test
public void shouldApplyDiscountForPremiumCustomer() {
    // Arrange
    Customer customer = new Customer("John", true);
    Order order = new Order(customer, 100);

    // Act
    order.applyDiscount();

    // Assert
    assertEquals(90, order.getTotal());
}
```

<!-- 
speaker_note: |
  A clear Arrange-Act-Assert structure helps you and others quickly understand the test’s purpose.
  If all three parts are blended together, debugging becomes harder.
-->

<!-- end_slide -->

Keep Tests Independent
===

- Tests should not depend on each other.
- One test failing should not cause a cascade.
- Use setup methods or builders to reduce duplication.

```java
@BeforeEach
public void setUp() {
    cart = new ShoppingCart();
}
```

<!-- 
speaker_note: |
  When tests depend on shared state or order of execution, they're fragile.
  Use clear setup logic to make each test standalone.
-->

<!-- end_slide -->

Don’t Include Logic in Tests
===

- Avoid loops, conditionals, or calculations in test code.
- Tests should be **declarative**, not **dynamic**.

```java
// ❌ Hidden logic
for (Item item : items) {
    cart.add(item);
}

// ✅ Be explicit
cart.add(item1);
cart.add(item2);
```

<!-- 
speaker_note: |
  Logic in tests can introduce bugs into your test suite.
  Keep tests flat and specific — they should state facts, not compute them.
-->

<!-- end_slide -->

Use Meaningful Names
===

- Test names should describe the scenario and the expected outcome.

```java
// ✅ Good
shouldReturnErrorWhenPasswordIsBlank()

// ❌ Bad
test1()
```

<!-- 
speaker_note: |
  A test name is the first line of defense when a test fails.
  Make it descriptive enough that you don’t have to read the body to understand the purpose.
-->

<!-- end_slide -->

Tests Should Be Fast
===

- Slow tests discourage frequent runs.
- Keep unit tests fast by avoiding:
  - Network calls
  - Disk I/O
  - Sleep or wait statements

<!-- 
speaker_note: |
  Fast tests give fast feedback.
  If tests are slow, developers run them less — and bugs slip through.
  Separate fast unit tests from slower integration or end-to-end tests.
-->

<!-- end_slide -->

Conclusion
===

- Clean tests are **fast**, **readable**, **independent**, and **specific**.
- They give you confidence to refactor and evolve your codebase.
- Don’t just write tests — craft them.

<!-- 
speaker_note: |
  Your tests should reflect the same care you give to your production code.
  Clear, reliable tests make your codebase safe to change — and a joy to work in.
  Next, we’ll explore classes — and how to keep them small, focused, and clean.
-->

<!-- end_slide -->

Chapter 10 — Classes
===

<!-- 
speaker_note: |
  Chapter 10 focuses on the structure and responsibility of classes.
  Uncle Bob's main advice: classes should be small, focused, and do one thing well.
-->

<!-- end_slide -->

Classes Should Be Small
===

- The smaller the class, the easier it is to understand.
- Aim for a **single responsibility**.
- A class should only have **one reason to change**.

<!-- 
speaker_note: |
  Think of classes like chapters in a book — each one should cover a single topic.
  If a class has multiple responsibilities, it’s harder to read, test, and maintain.
-->

<!-- end_slide -->

The Single Responsibility Principle
===

- A class should **do one thing**.
- It should have **one reason to change**.

```java
// ❌ Violates SRP: two responsibilities
public class UserManager {
    public void createUser(User u) {...}
    public void saveToDatabase(User u) {...}
}

// ✅ Better: split responsibilities
public class UserCreator {
    public void createUser(User u) {...}
}

public class UserRepository {
    public void save(User u) {...}
}
```

<!-- 
speaker_note: |
  When a class has more than one reason to change, it’s harder to manage.
  Breaking it into smaller, purpose-driven classes improves clarity and flexibility.
-->

<!-- end_slide -->

Cohesion
===

- High cohesion = methods and variables are closely related.
- All methods should operate on the same subset of data.
- Low cohesion means the class likely does too much.

<!-- 
speaker_note: |
  A cohesive class feels tight — its methods work together toward a single goal.
  If methods feel unrelated, that’s a sign the class needs to be split.
-->

<!-- end_slide -->

Organizing Class Structure
===

- Use a consistent order:
  - Public methods first
  - Private helpers after
- Group related methods together.

```java
public class Invoice {
    public void print() {...}
    public double getTotal() {...}

    private double calculateTax() {...}
    private void formatLineItem(Item item) {...}
}
```

<!-- 
speaker_note: |
  Code readers expect structure. Put the public-facing parts up top.
  Keep private helpers below to avoid distraction.
-->

<!-- end_slide -->

Classes Should Be Focused
===

- Don’t turn classes into "God objects."
- One class per concept — not one class for the whole feature.

```java
// ❌ Bloated
public class OrderManager {
    // business logic
    // persistence logic
    // formatting
}

// ✅ Focused
public class OrderProcessor {...}
public class OrderRepository {...}
public class OrderFormatter {...}
```

<!-- 
speaker_note: |
  When one class knows too much or does too much, it's hard to test and change.
  Divide responsibilities and assign them to clear, focused roles.
-->

<!-- end_slide -->

Conclusion
===

- Keep classes **small**, **cohesive**, and **focused**.
- Apply the Single Responsibility Principle.
- A clean class is like a clean function — it tells one story.

<!-- 
speaker_note: |
  Classes are the next level up from functions. If your functions are clean but your classes are bloated, you still have a problem.
  Use the same discipline: clarity, purpose, and minimal responsibility.
  Next up: systems — how clean classes fit into clean architectures.
-->

<!-- end_slide -->

Chapter 11 — Systems
===

<!-- 
speaker_note: |
  Chapter 11 zooms out from classes and functions to the system level.
  Clean systems are just as important as clean code — because systems define how pieces fit and work together.
-->

<!-- end_slide -->

Separate Construction from Use
===

- Objects should be constructed separately from how they’re used.
- Don’t mix wiring logic with business logic.
- Use **factories**, **dependency injection**, or frameworks to manage creation.

```java
// ❌ Mixed construction and logic
public void handleRequest() {
    Service service = new Service(new Repository());
    service.process();
}

// ✅ Construction elsewhere
public class Handler {
    private final Service service;
    public Handler(Service service) {
        this.service = service;
    }
    public void handleRequest() {
        service.process();
    }
}
```

<!-- 
speaker_note: |
  Construction and business logic are different concerns.
  Separating them makes your system easier to test, configure, and extend.
-->

<!-- end_slide -->

Use Dependency Injection
===

- Inject dependencies rather than creating them.
- Promotes loose coupling and testability.

```java
public class BillingService {
    private final PaymentGateway gateway;
    
    public BillingService(PaymentGateway gateway) {
        this.gateway = gateway;
    }

    public void charge(Customer c) {...}
}
```

<!-- 
speaker_note: |
  When your classes depend on abstractions passed in from the outside, they become easier to substitute and mock.
  This makes unit testing much simpler and your code more flexible.
-->

<!-- end_slide -->

Keep the Main Flow Clean
===

- The primary use cases should read like a script.
- Hide wiring, setup, and framework code in the background.

```java
public void placeOrder() {
    validateInput();
    processPayment();
    updateInventory();
    notifyCustomer();
}
```

<!-- 
speaker_note: |
  Just like clean functions, clean systems tell a clear story.
  Don’t bury the main flow in technical noise — highlight what matters most.
-->

<!-- end_slide -->

Use Plugins and Extension Points
===

- Treat volatile parts of the system as **plugins**.
- Define stable interfaces that can be swapped or extended.

```java
public interface NotificationService {
    void send(String message);
}

public class EmailNotification implements NotificationService {
    public void send(String message) {...}
}
```

<!-- 
speaker_note: |
  Anything that’s likely to change — like notifications, storage, or APIs — should be isolated behind an interface.
  That way, the rest of the system stays stable.
-->

<!-- end_slide -->

Separate Policies from Details
===

- Policies = business rules.
- Details = frameworks, databases, UIs, etc.
- Keep your core logic independent from technology choices.

```java
// Policy (business logic)
public class ShippingCalculator {
    public double calculate(Order order) {...}
}

// Detail (API integration)
public class FedExAdapter {
    public void ship(Order order) {...}
}
```

<!-- 
speaker_note: |
  Business logic should not care how data is stored or transmitted.
  Keep the core of your system focused on solving real problems — not the tools used to do it.
-->

<!-- end_slide -->

Conclusion
===

- Clean systems are loosely coupled, clearly structured, and easy to evolve.
- Separate construction, wiring, and framework code from business logic.
- Design your system like a story — clear and purposeful.

<!-- 
speaker_note: |
  System-level clean code matters just as much as clean methods or classes.
  Keep the core focused, flexible, and protected from volatile dependencies.
  Next up: emergent design — how good structure evolves from good practices.
-->

<!-- end_slide -->

Chapter 12 — Emergent Design
===

<!-- 
speaker_note: |
  In Chapter 12, Uncle Bob presents how good design can emerge from following a few core practices consistently.
  You don’t always need a perfect architecture upfront — you can grow it as the system evolves.
-->

<!-- end_slide -->

Four Rules of Simple Design
===

1. Passes all the tests
2. Contains no duplication
3. Expresses the programmer’s intent
4. Minimizes the number of classes and methods

<!-- 
speaker_note: |
  These four rules help guide emergent design — design that grows as your code evolves.
  When applied consistently, they naturally push your code toward clarity and simplicity.
-->

<!-- end_slide -->

Pass All Tests
===

- Tests are the foundation of confidence.
- Design must support testability.
- Without tests, refactoring becomes risky.

```java
@Test
public void calculatesTotalPrice() {
    assertEquals(15.0, cart.total());
}
```

<!-- 
speaker_note: |
  Clean design starts with reliable tests.
  If you can’t test it easily, it’s probably not well-designed.
-->

<!-- end_slide -->

Eliminate Duplication
===

- DRY (Don’t Repeat Yourself) principle is key.
- Duplication hides bugs and increases maintenance.

```java
// ❌ Duplication
calculateTax(usRate);
calculateTax(usRate);

// ✅ Extracted method
applyStandardTax();
```

<!-- 
speaker_note: |
  Duplication often signals a missing abstraction.
  If you see the same logic or structure in multiple places, pull it out and name it.
-->

<!-- end_slide -->

Express Intent Clearly
===

- Code should clearly express what it does.
- Prefer clarity over cleverness.
- Names, structure, and flow should make purpose obvious.

```java
// ❌ Unclear
if (d < 86400000) {...}

// ✅ Clear
if (durationInMs < ONE_DAY_IN_MS) {...}
```

<!-- 
speaker_note: |
  You shouldn’t need comments to understand intent — the code itself should say it.
  Use clear names and structure that match how you’d explain it to a teammate.
-->

<!-- end_slide -->

Minimize Classes and Methods
===

- Don’t over-engineer.
- Fewer, focused classes and methods are easier to maintain.

```java
// ❌ Over-abstracted
interface PriceStrategy {...}
class StandardPrice implements PriceStrategy {...}
class PremiumPrice implements PriceStrategy {...}

// ✅ Simple when requirements are stable
class PriceCalculator {
    public double calculate(Order order) {...}
}
```

<!-- 
speaker_note: |
  Abstraction is good — but too much, too early can hurt clarity.
  Keep it simple until complexity justifies more structure.
-->

<!-- end_slide -->

Refactor Continuously
===

- Refactoring is the engine of emergent design.
- Always clean as you go.
- Small, safe improvements compound over time.

<!-- 
speaker_note: |
  Design isn’t just planning — it’s something you *do* while coding.
  Refactor constantly to keep your code lean, expressive, and adaptable.
-->

<!-- end_slide -->

Conclusion
===

- Good design emerges from small, consistent actions.
- Follow the four rules of simple design.
- Clean code grows, adapts, and improves continuously.

<!-- 
speaker_note: |
  Don’t wait for the big refactor. Don’t chase the perfect design upfront.
  Write tests, remove duplication, express intent, and keep things minimal.
  In the final chapter, we’ll look at how the disciplines of clean code tie into professional ethics.
-->

<!-- end_slide -->

Chapter 13 — Concurrency
===

<!-- 
speaker_note: |
  In Chapter 13, Uncle Bob discusses how to handle concurrency — one of the most complex aspects of software development.
  The goal is to manage multiple threads cleanly, safely, and with minimal pain.
-->

<!-- end_slide -->

The Benefits and Risks of Concurrency
===

- ✅ Enables responsive UIs and scalable systems
- ⚠️ Introduces complexity, race conditions, deadlocks
- Must be approached with caution and clarity

<!-- 
speaker_note: |
  Concurrency can improve performance, but it also creates opportunities for bugs that are hard to reproduce and debug.
  It’s powerful — but only when used with care.
-->

<!-- end_slide -->

Single Responsibility Applies to Threads
===

- Each thread should have **one job**
- Avoid mixing responsibilities across threads

```java
// ❌ One thread doing too much
Thread t = new Thread(() -> {
    authenticate();
    loadUserData();
    logAccess();
});

// ✅ Better separation
Thread authThread = new Thread(this::authenticate);
Thread dataThread = new Thread(this::loadUserData);
```

<!-- 
speaker_note: |
  Just like classes and functions, threads should do one thing well.
  Mixing unrelated actions in one thread makes debugging harder.
-->

<!-- end_slide -->

Encapsulate Thread Management
===

- Hide threading logic behind clear abstractions
- Don’t scatter `Thread` or `Executor` calls everywhere

```java
public class TaskRunner {
    private final Executor executor;

    public TaskRunner(Executor executor) {
        this.executor = executor;
    }

    public void runAsync(Runnable task) {
        executor.execute(task);
    }
}
```

<!-- 
speaker_note: |
  Keep thread management behind a simple interface.
  It’s easier to maintain, test, and change your concurrency model later if it’s well-encapsulated.
-->

<!-- end_slide -->

Use Messaging to Avoid Shared State
===

- Shared mutable state is a source of bugs
- Prefer queues, messages, and tasks to direct state sharing

```java
BlockingQueue<Event> queue = new LinkedBlockingQueue<>();

// Producer
queue.put(new Event("click"));

// Consumer
Event event = queue.take();
```

<!-- 
speaker_note: |
  Whenever possible, use message passing rather than shared variables.
  This reduces coupling and makes your concurrent system safer and easier to understand.
-->

<!-- end_slide -->

Know Your Synchronization Primitives
===

- Understand tools like:
  - `synchronized`
  - `volatile`
  - `ReentrantLock`
  - `Semaphore`, etc.
- Use the simplest tool that works for the job

<!-- 
speaker_note: |
  Don’t overuse `synchronized` or `locks` without understanding them.
  Know what guarantees each primitive provides — and choose based on need, not habit.
-->

<!-- end_slide -->

Test Concurrent Code Carefully
===

- Concurrency bugs are **timing-sensitive**
- Use thread stress tests, race condition checks, and monitoring
- Tools: thread sanitizers, profilers, log tracing

<!-- 
speaker_note: |
  Concurrency issues often hide until just the wrong moment.
  Use dedicated tools and stress tests to surface problems early.
-->

<!-- end_slide -->

Keep It Simple
===

- Concurrency is risky — use only when necessary
- Don’t add threads or locks unless there’s a clear benefit

<!-- 
speaker_note: |
  Every thread is a point of failure.
  Start with the simplest design and add concurrency only where you need performance gains.
-->

<!-- end_slide -->

Myths and Misconceptions
===

- ❌ Concurrency always improves performance — sometimes it adds overhead
- ❌ Synchronized code is always safe — it might still deadlock or starve
- ❌ Threads are the only way to scale — alternatives exist (e.g., async I/O, reactive programming)
- ✅ Correctness comes first — performance follows

<!-- 
speaker_note: |
  Uncle Bob closes the chapter by addressing common concurrency myths.
  The truth is: concurrency is hard, and it doesn’t solve every problem.
  Always prioritize correctness, simplicity, and safety.
-->

<!-- end_slide -->

Conclusion
===

- Concurrency enables power and performance — but brings risk
- Encapsulate thread logic, avoid shared state, and test thoroughly
- Simple, focused design principles still apply

<!-- 
speaker_note: |
  Clean concurrent code is possible — it just takes more discipline.
  Stick to small, clear responsibilities. Encapsulate complexity. And always, always test under pressure.
  Next, we’ll wrap up with professional practices — what it really means to be a clean coder.
-->

<!-- end_slide -->


Chapter 14 — Successive Refinement
===

<!-- 
speaker_note: |
  The final chapter of Clean Code is a walkthrough — showing how messy code becomes clean through careful, disciplined refinement.
  It’s an opportunity to watch clean code principles in action, step by step.
-->

<!-- end_slide -->

Start with Working Code
===

- The example begins with a function that works but is messy
- It’s long, unclear, and has duplication
- Goal: preserve behavior while improving structure

<!-- 
speaker_note: |
  Uncle Bob starts with a real example — a function that technically works, but clearly violates clean code principles.
  He shows that clean code is a process, not a one-time event.
-->

<!-- end_slide -->

Refactor in Small Steps
===

- Make small, safe changes
- Keep the code compiling and tests passing
- Refactor one concept at a time

```java
// ❌ Mixed concerns
parseAndValidate(input);
updateState();
log(input);

// ✅ Refactor one step
parseInput(input);
validateInput(input);
```

<!-- 
speaker_note: |
  Don’t try to clean everything at once. Work incrementally.
  Rename things, extract methods, clarify intent — always one safe change at a time.
-->

<!-- end_slide -->

Extract Functions to Reveal Intent
===

- Break large blocks into named methods
- Names should say *why*, not *how*

```java
// ❌ Hidden meaning
if (user.age > 65 && user.hasInsurance()) {...}

// ✅ Clear intent
if (isEligibleForSeniorCoverage(user)) {...}
```

<!-- 
speaker_note: |
  Good method names reduce the need for comments and improve understanding.
  Naming is the bridge between messy logic and clear thought.
-->

<!-- end_slide -->

Remove Duplication
===

- Duplication is a major source of bugs
- Refactor repeated logic into common functions

```java
// ❌ Repeated
if (status.equals("active") && role.equals("admin")) {...}

// ✅ Consolidated
if (isPrivilegedUser(user)) {...}
```

<!-- 
speaker_note: |
  Duplication means more places to change when requirements evolve.
  Find the commonality and extract it — your future self will thank you.
-->

<!-- end_slide -->

Focus on Expressiveness
===

- Clean code is **clear** before it is **efficient**
- Make it readable, then optimize if needed

```java
// ❌ Cryptic
int x = 86400000;

// ✅ Expressive
int ONE_DAY_IN_MS = 86400000;
```

<!-- 
speaker_note: |
  Code is read more than it’s written — and it’s read by humans.
  Make your intent obvious. Performance comes later, and often isn’t affected by clarity.
-->

<!-- end_slide -->

Final Refinement: From Mess to Message
===

- By the end, the code is short, expressive, and intention-revealing
- All principles come together:
  - Small functions
  - Meaningful names
  - No duplication
  - Clean structure

<!-- 
speaker_note: |
  The final version of the code isn’t just correct — it’s beautiful.
  It communicates intent clearly and feels effortless to read.
  That’s the power of successive refinement.
-->

<!-- end_slide -->

Conclusion
===

- Clean code doesn’t start clean — it gets there through discipline
- Refactor constantly
- Make clarity your default goal

<!-- 
speaker_note: |
  Writing clean code isn’t a magical skill — it’s a habit.
  The more you refine, the cleaner your code becomes.
  And that’s what separates great developers from average ones.
-->

<!-- end_slide -->


