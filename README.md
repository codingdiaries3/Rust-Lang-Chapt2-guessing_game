### Notes

1. stdin() is standard in

2. std::io is a library that provides a feature to accept user input

3. The io library comes from the standard library which is known as std that is part of rust

4. String::new() is a function that returns a new instance of a String.
   The word "new" can be called anything but its convention to use "new".

5. Immutable/Mutable\
   Mutable means the variable can change its value\
   Immutable means the variable can't be changed

   ```
   let foo = 5; // immutable
   let mut bar = 5; // mutable
   ```

6. The `.read_line()` returns 1 of 2 results, 'ok' or 'error' and the `expect` function handles the values that were returned.

7. Using `expect` crashes the program when there is an error. There are better ways to handle errors but for now `expect` is being used.

8. In `println("You guessed: {}", guess)` the curly brackets is a placeholder.\

   ```
   let x = 5;
   let y = 10;

   println!("x = {} and y = {}", x, y);
   ```

   Any time you want to a variable to pass, you write out the string and use curly brackets as a placeholder to the variable and add the variables at the end.

9. Update Command

   ```
   cargo update
   ```

   When updating version, the update command will only update to the latest 0.8.x. If you want to update to a 0.9.x version you will have to specify that in the dependencies in Cargo.toml file then run `cargo build` and cargo will update to the new version you specified.

10. You won’t just know which traits to use and which methods and functions to call from a crate. Instructions for using a crate are in each crate’s documentation.You can run the `cargo doc --open` command, which will build documentation provided by all of your dependencies locally and open it in your browser. For example, if you’re interested in other functionality in the rand crate run `cargo doc --open` and click rand in the sidebar on the left.

11. thread_rng() gives a particular random number. To request numbers between 1 to 100 the end digit should either be written as gen_range(1..101) or gen_range(1..=100). gen_range(start..end).

12. Ordering is an enum and the variants for Ordering are Less, Greater, and Equal. These are the three outcomes that are possible when comparing to values.

13. The cmp method compares two values and can be called on anything that can be compared. In this project its comparing the guess variable to the secret_number variable. Then it uses the Ordering enum variant.

14. Using the match expression.\
    Rust takes the value given to match and looks through each arm's pattern. Then it runs the code if it matches the pattern.

15. Rust numerical types defaults to i32 unless you add type information.(e.g. u32,i64, etc)

16. To convert a value from one type to another type you can shadow the previous value. Shadowing lets us reuse the variable name rather than forcing us to create two unique variables. Like in our guessing game, the "guess" variable was set to be a string (line 12)and then later down the code (line 18)we set it to be a number.

17. The trim method on a string instance eliminates any whitespace at the beginning and end.

18. The parse method on strings parses a string into some kind of number. This method can parse a variety of number types so we need to specify the exact number type we want. Parse uses the Result type, it will return the 'Err' or 'ok' variant depending on whether it was able to parse what was given to it or not.

19. In line 22, the underscore in Err is a catchall value. Meaning it'll match all Err values no matter what information it has. The continue keyword telss the program to go to the next iteration of the loop.
