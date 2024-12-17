## first section
--dealt with installation and coding basic rust files.

# Setting up a new project
1. ```bash
    cargo new project_name
    ```

# For getting help with Rust
1. ```bash
    rustup doc
    ```
    (to see the documentation of Rust).

# Keypoints:
1. rustup updates the version of Rust, helps in uninstalling Rust.
2. Method calls from libraries like `println` are called macros here.
3. In Rust, all macros have an exclamation mark `!`.
4. `rustc` is Rust's compiler.

# Running Rust using rustc as a command line program
1. ```bash
    rustc main.rs
    ```
2. ```bash
    ./main.exe
    ```

# Formatting with rustfmt and cargofmt
1. `rustfmt` will format the code as per how the designers thought Rust code should look, whereas `cargofmt` is about community standards.
2. To use rustfmt:
    ```bash
    rustfmt main.rs
    ```
    (This has to be run in the directory where the file is present)
3. To use cargofmt:
    ```bash
    cargo fmt
    ```
    (this command can format the entire project directory when run from the project directory)

# The cargo build command
1. Earlier we used `rustc` to compile a particular `.rs` file, whereas cargo can be used to compile the entire project.
2. ```bash
    cargo build
    ```
    compiles all of the project files to executables.
3. We can build or compile the final application in one of two modes: Debug and Release mode. By default, `cargo build` runs in debug mode.
4. Debug vs Release mode:
    a. Debug is a fast and unoptimized build. This kind of compilation generates meta files that help developers to debug. (`/target/debug`)
    b. To get the final files, we compile in release mode. It is optimized for runtime performance. The final executable is slower than that of debug mode.
5. ```bash
    cargo build
    ```
    (you will see new files being generated in `target/debug`)
6. To build with release mode:
    ```bash
    cargo build --release
    ```
    and it will put the files in the `/target/release` directory.
7. To clean (delete all the compiled files), use:
    ```bash
    cargo clean
    ```
    it will delete the entire target folder.
8. ```bash
    cargo build
    ```
    is equivalent to
    ```bash
    cargo b
    ```

# Running Rust using the "Run" button
1. This will create a new directory `target`. It's equivalent to build (`cargo build`).

# cargo run command
1. Instead of building `.exe` files and then running them manually, we can do both steps with a single command:
    ```bash
    cargo run
    ```
2. Same as the "Run" button.
3. To see only the output of the build (without Compiling, Finished, Running steps being shown), add a `--quiet` flag:
    ```bash
    cargo run --quiet
    ```
4. ```bash
    cargo run
    ```
    is equivalent to
    ```bash
    cargo r
    ```

# The cargo check command
1. The check command checks the source code for any compiler violations but does not produce any executables.
2. It's like a mock run.
3. ```bash
    cargo check
    ```

# Conclusion:
1. Compiler - `rustc`
2. Project manager - `cargo`
3. Utility tools (rustup + rustfmt)
4. Function names have to be in snake_case. section
