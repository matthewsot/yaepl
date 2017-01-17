# CSS-Yaepl
Mimics CSS syntax.

- Target of action is declared first
- Property, or type of action, is then declared
- Finally, value or parameters of action is declared

## Hello, World!
```
my-string {
    create-variable: String;
    set-value: "Hello, World!";
}
my-string-length {
    create-variable: number;
}
my-string {
    store-length: my-string-length;
}
output {
    write: my-string;
    write: my-string-length;
}
```

## Pros/Cons
Pros:
- Extremely simple to explain the basic syntax for creating and operating on objects (say the object name, then what you want to do, then specify the value for that thing you want to do).

Cons:
- Very clunky very fast.
- This syntax makes sense for CSS because it is only doing one thing: modifying object properties. That doesn't really translate to something like Javascript.