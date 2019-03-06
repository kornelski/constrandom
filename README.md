# Random constants
This crate provides compile time random number generation.
This allows you to insert random constants into your code that will be auto-generated at compile time.

A new value will be generated every time the file is rebuilt.
This obviously makes the resulting binary or lib non-deterministic.

# Example 

```
use const_random::const_random  ;
const MY_RANDOM_NUMBER: u32 = const_random!(u32);
```
This works exactly as through you have called: `rand::random::<u32>()` except that code is being run at compile time.
So for details of the random number generation, see the `rand` crates documentation.

The following types are supported: u8, i8, u16, i16, u32, i32, u64, i64, u128. i128.

----

[![xkcd: chosen by fair dice roll](https://imgs.xkcd.com/comics/random_number.png)](https://xkcd.com/221/)
