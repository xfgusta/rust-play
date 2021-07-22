# rust-play

A [Rust Playground](https://play.rust-lang.org/) CLI client

## Examples

```
$ rsplay < examples/add.rs
3
```

```
$ rsplay -s < examples/love.rs
ID: 3efd14d55cbbbb72b7032a170b4d9348
Playground: https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=3efd14d55cbbbb72b7032a170b4d9348
Gist: https://gist.github.com/rust-play/3efd14d55cbbbb72b7032a170b4d9348
```

```
$ rsplay -g 3efd14d55cbbbb72b7032a170b4d9348
fn main() {
    for _ in 1..=100 {
        println!("I love Rust");
    }
}
```

```
$ rsplay -r 3efd14d55cbbbb72b7032a170b4d9348
I love Rust
I love Rust
I love Rust
I love Rust
I love Rust
[...]
```

```
$ cat examples/ferris.rs | rsplay
   Compiling playground v0.0.1 (/playground)
error[E0423]: expected function, found macro `println`
 --> src/main.rs:2:5
  |
2 |     println("Ferris");
  |     ^^^^^^^ not a function
  |
help: use `!` to invoke the macro
  |
2 |     println!("Ferris");
  |            ^

error: aborting due to previous error
[...]
```

Use `rsplay -h` for more options.

## License

The MIT License (MIT)

Copyright (c) 2021 Gustavo Costa
