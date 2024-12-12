# Rewriting a Python Script in Rust: Analysis of Spotify 2023 Streaming Data

## Introduction

This repository showcases a comparison between a data processing script in Python and its equivalent in Rust. The main goal is to illustrate the enhancements in speed and resource efficiency when using Rust.

## Installation Guide

### Installing Rust

If Rust is not installed on your machine, you can easily get it using Rustup. Rustup is the recommended installation tool for Rust and it also installs Cargo. Run the following command in your terminal or command prompt:

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs/ | sh
```

### Setting Up a New Rust Project

If you need to create a new Rust project, you can use Cargo, Rust's build tool and package manager. Use the following command in your terminal:

```
cargo new rust_spotify_analysis
```

This command will create a new Rust project called `rust_spotify_analysis`, generating a directory structure with a `Cargo.toml` file (for project metadata and dependencies) and a `src` directory (for the source code).

### Adding Rust Code

Go to the `rust_spotify_analysis` directory and open the `src` folder. You'll find a `main.rs` file here, which is the main entry point of your Rust project. Copy and paste your Rust code into this file.

### Adding Dependencies

In the `Cargo.toml` file, you'll need to specify dependencies for your project. Add the necessary libraries under the `[dependencies]` section, such as `csv`, `polars`, and `plotters`:

```
[dependencies]
csv = "1.1"
polars = "0.14"
plotters = "0.3"
```

Ensure to check for the latest versions on Cargo's crate registry as version numbers might vary.

### Running Your Rust Code

To compile and run the Rust code, open a terminal in your project's root directory (where `Cargo.toml` is) and run:

```
cargo run
```

For an optimized release build, use:

```
cargo run --release
```

## Rust vs Python: Performance and Resource Utilization

### General Information

- **Python Script:** Processes Spotify data using pandas and seaborn.
- **Rust Script:** Uses rust-csv, polars, and plotters for data processing and visualization.

### Setup and Execution

#### Python

**Prerequisites:**

- Python 3.x
- pandas
- seaborn

Install and run with:

```
pip install pandas seaborn
python script_name.py
```

#### Rust

**Prerequisites:**

- Rust and Cargo

Build and run with:

```
cargo build --release
cargo run --release
```

### Performance and Resource Utilization

Both scripts were evaluated using the same dataset. Detailed performance results are available in the report.

**Key Points:**

- **Execution Time:** The Rust version significantly improves the execution speed compared to the Python version.
- **Memory Usage:** The Rust version demonstrates more efficient memory usage than the Python version.

## Conclusion

This project underscores the benefits of using Rust for data processing, particularly in terms of performance and resource efficiency. While Python is user-friendly and has a broad range of data science libraries, Rust offers substantial performance advantages, making it suitable for more demanding tasks.
