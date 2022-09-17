# Visual Studio

## Useful Notes
* To checkout the compiled machine code of a C# build, run the `ildasm` on the terminal
    * You will see what methods, functions, properties, etc. eventually turned into.
    * Example:
    ```csharp
        public string Name {get; set;}
    ```
    By running `ildasm` command, you can see the compiler automatically creates a private field and getter a getter and setter methods

## Useful Visual Studio Keyboard Shortcuts

#### Comment: `Ctrl + k, c`
#### Undo Comment: `Ctrl + k, u`
#### Run Test With Debugger: `Ctrl + r, Ctrl + a`
#### Run Test Without Debugger: `Ctrl + r, a`
#### Run Invividual Test: `Ctrl + r, t`
#### Auto-Complete/Code Suggestions: `Ctrl + .`
#### Go To Definition: `F12`
#### Peek Definition: `Alt + F12`
#### Replace: `Ctrl + H`