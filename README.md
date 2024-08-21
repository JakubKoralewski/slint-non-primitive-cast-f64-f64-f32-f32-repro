cargo generate --git https://github.com/slint-ui/slint-rust-template --init -n x -o

```
cargo run
   Compiling slint-non-primitive-cast-f64-f64-f32-f32-repro v0.1.0 (D:\...\slint-non-primitive-cast-f64-f64-f32-f32-repro)
error[E0605]: non-primitive cast: `(f64, f64)` as `(f32, f32)`
   --> D:\...\slint-non-primitive-cast-f64-f64-f32-f32-repro\target\debug\build\slint-non-primitive-cast-f64-f64-f32-f32-repro-1d21787b4cb0939a\out\appwindow.rs:466:14
    |
466 | /              ({
467 | |                  (0f64 , 100f64 ,) }
468 | |             ) as _ }
    | |__________________^ an `as` expression can only be used to convert between primitive types or to coerce to a specific trait object

For more information about this error, try `rustc --explain E0605`.
error: could not compile `slint-non-primitive-cast-f64-f64-f32-f32-repro` (bin "slint-non-primitive-cast-f64-f64-f32-f32-repro") due to 1 previous error
```

```
> rustup toolchain list
nightly-x86_64-pc-windows-msvc (default)
> cargo --version
cargo 1.82.0-nightly (2f738d617 2024-08-13)
> rustc --version
rustc 1.82.0-nightly (506052d49 2024-08-16)
> ver
Microsoft Windows [Version 10.0.19045.4780]
```

Same on stable
```
> rustup toolchain list
stable-x86_64-pc-windows-msvc (default)
> rustc --version
rustc 1.80.1 (3f5fd8dd4 2024-08-06)
> cargo --version
cargo 1.80.1 (376290515 2024-07-16)
```

Same on WSL
```
$ rustup toolchain list
stable-x86_64-unknown-linux-gnu (default)
$ rustc --version
rustc 1.80.1 (3f5fd8dd4 2024-08-06)
$ cargo --version
cargo 1.80.1 (376290515 2024-07-16)
$ uname -a
Linux DESKTOP-NI12FI7 5.15.133.1-microsoft-standard-WSL2 #1 SMP Thu Oct 5 21:02:42 UTC 2023 x86_64 x86_64 x86_64 GNU/Linux
```
