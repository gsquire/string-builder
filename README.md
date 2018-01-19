# string-builder
[![Build Status](https://travis-ci.org/gsquire/string-builder.svg?branch=master)](https://travis-ci.org/gsquire/string-builder)

This crate is a simple string builder type allowing you to append anything that satisfies the
`ToBytes` trait to it. This includes things such as string slices, owned strings, byte slices,
and characters for example.

## Example
```rust
extern crate string_builder;

use string_builder::Builder;

fn main() {
    let mut b = Builder::default();
    b.append("it");
    b.append(' ');
    b.append("works!");

    assert_eq!(b.string().unwrap(), "it works!");
}
```
## License
MIT
