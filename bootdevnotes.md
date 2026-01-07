# Boot dev notes

## Python
* **print("hello world")**
* **var** = integer, "String", fl.oat, boolean (T or F)
* **snake_case** for var names
- f-string for dynamic values (E.g. bananas = f"You have {num_bananas} bananas")
- set NoneType for empty (absence of a value)
- save space by declaring multiple vars on same line (E.g. name, damage, length = "Excalibur", 10, 20)
- Function declared as:
    '''python
    def function_name(input1, input2, ...):
        blah
        if/elif, for, while, etc
        return result1, result2, ... (end var you want to pass out)
        '''

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

- Math is pretty straight forward, + - * /
    *EXCEPT*
    Dividing two integers produces a float
        In comes Floor Division (amazing)
            7 // 3 = 2, result is "floored", or rounded down to nearest integer

    Exponent = 3 ** 2 = 9

    In-place operators
        var += 1, -= 1, *= 1, /=1
        Increments var by whatever is decided

    Scientific Notation
        print(16e3)
        num = 16_000, underscore as "delimiter" for easier readability

- Logical Operators
    Can be nested

    True and True == True
    True and False == False
    False and False == False

    True or True == True
    True or False == True
    False or False == False

- The not operator reversed the result
    not True = False

- Binary
    print(0b0101) = 5

    Bitwise & (and, ampersand) operator:
    0101
    &
    0111
    =
    0101

    | (or) operator:
    0101
    |
    0111
    =
    0111

    Useful for something like guild permissions:
        can_create_guild - Leftmost bit (0b1000)
        can_review_guild - Second to leftmost bit (0b0100)
        can_delete_guild - Second to rightmost bit (0b0010)
        can_edit_guild - Rightmost bit (0b0001)

    Converting:
        int() function converts binary string to an integer
        binary_string = "100"
        num = int(binary_string, (base goes in this slot) 2)

- Boolean Logic
    Compares two values, result is either True or False

- if statements:
    Useful to only execute code if a certain condition is met
        def show_status(boss_health):
            if boss_health > 0:
                print("Ganondorf is alive!")
                return
            print("Ganondorf is unalive!")

    Can be followed by zero or more elif (else if) statements, which can be followed by zero or one else statements
    def player_status(health):
        if health <= 0:
            return "dead"
        elif health <= 5:
            return "injured"
        else:
            return "healthy"

    Determine if bartender shouls serve drinks to customer. Only return TRUE if *all* conditions apply:
    def should_serve_customer(customer_age, on_break, time):
        if customer_age < 21:
            return False
        if on_break (== TRUE is redundant here) :
            return False
        if time < 5 or time > 10:
            return False
        return True

- Loops!!!
    Same operation multiple times without rewriting code explicitly each time
    
    FOR loops
    Prints numbers 0 to 9:
        for i in range(0, 10):
            print(i)
    range(start, end, step), can go backwards, range(end, start, -1)
    
    Sum of odd numbers:
        def sum_of_odd_numbers(end):
            total = 0
            for i in range(1, end, 2):
                total += i
            return total

    WHILE loops
        def regenerate(current_health, max_health, enemy_distance):
            while current_health < max_health and enemy_distance > 3:
                current_health += 1
                enemy_distance -= 2
            return current_health

    CONTINUE statement
    Means "go directly to the next iteration of this loop"
        def award_enchantments(start, end, step):
            counter = 0

            for quest_number in range(start, end, step):
                counter = counter + 1
                if counter < 3:
                    continue

                counter = 0
                enchantment_strength = quest_number * 5
                print(
                    f"Enchantment of strength {enchantment_strength} awarded for completing {quest_numbe                    r} quests!"
                )

    BREAK statement
    Exit the loop
        for n in range(42):
            print(f"{n} * {n} = {n * n}")
            if n * n > 150:
                break

-CH 9
