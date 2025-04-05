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
