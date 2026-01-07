# Boot dev notes

# Python
- print("hello world")
- var = integer, "String", fl.oat, boolean (T or F)
- snake_case for var names
- f-string for dynamic values (E.g. bananas = f"You have {num_bananas} bananas")
- set NoneType for empty (absence of a value)
- save space by declaring multiple vars on same line (E.g. name, damage, length = "Excalibur", 10, 20)
- Function declared as:
    def function_name(input1, input2, ...):
    blah
    if/elif, for, while, etc
    return result1, result2, ... (end var you want to pass out)

- Call using function = function_name(input1, ...)
- print() is a function that:
    Prints a value to the console
    Does not return a value
- return is a keyword that:
    Ends the current function's execution
    Provides a value (or values) back to the caller of the function
    Does not print anything to the console (unless the return value is later print()ed)

- All functions *MUST* be defined *BEFORE* they're used
- Entry point function
    def main()
    blah
    blah

- Call entry point last
    main()

- Arguments are actual values
- Parameters are the names
- Default values nice for parameters that are "optional" 
    def get_greeting(email, name="there"):
        print("Hello", name, "welcome! You've registered your email:", email)

- CH4
