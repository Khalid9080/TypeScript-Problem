# TypeScript-Problem
## Question-03: Explain the difference between any, unknown, and never types in TypeScript.

✅ Difference Between any, unknown, and never in TypeScript

🔹 any
- The most flexible and least safe type.
- Tells TypeScript to stop checking the type.
- Anything can be assigned to it.
- Operations on it are allowed without restrictions.
- Useful when migrating old JS code, but risky for type safety.

🔹 unknown
- Similar to any because it can hold any value.
- BUT unlike any, you cannot use it directly.
- You must check its type before performing operations.
- Much safer than any.
- Best for user inputs, API responses, or values coming from external sources.

🔹 never
- Represents a value that never occurs.
- Used for functions that never return (e.g., always throws error or loops forever).
- Also used in exhaustive checks to ensure all cases are handled.
- Nothing can be assigned to never.

| Type        | Meaning                                 | Safety Level | When to Use                         |
| ----------- | --------------------------------------- | ------------ | ----------------------------------- |
| **any**     | Anything allowed, no checks             | ❌ Least safe | Temporary escape from type checking |
| **unknown** | Any value, but must validate before use | ✔ Safer      | Handling uncertain or external data |
| **never**   | Impossible value, never returns         | ✔✔ Very safe | Error functions, exhaustive checks  |





## Question-04: What is the use of enums in TypeScript? Provide an example of a numeric and string enum.

✅ What is the use of enums in TypeScript?

Enums in TypeScript are used to define a group of related constant values under a single meaningful name.
They help make code:

- More readable
- Less error-prone
- Easier to maintain

More descriptive than using raw numbers or strings. Enums are especially useful when certain values represent fixed categories, such as user roles, directions, statuses, or modes. They prevent "magic numbers" or repeated string literals and also provide TypeScript’s type safety by restricting values to a predefined set.

✅ Numeric Enum (Description)
A numeric enum is an enum where the constant values are numbers.
The numbers may start from zero or any custom number.
If a starting number is given, the next values automatically increase by 1.

Use cases:
- Directions (Up, Down, Left, Right)
- Levels (Beginner, Intermediate, Advanced)
- Status codes
  
```
enum Direction {
  Up = 1,
  Down,
  Left,
  Right
}

```

✅ String Enum (Description)
A string enum is an enum where each constant value is a string.
Every value must be explicitly written because strings do not auto-increment like numbers.

Use cases:
- User roles (Admin, Editor, Viewer)
- API status ("SUCCESS", "ERROR", "LOADING")
- Categories that must be human-readable

```
enum Status {
  Success = "SUCCESS",
  Error = "ERROR",
  Pending = "PENDING"
}

```
