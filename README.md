# otter-test
Standard library package for Otter providing unit testing assertions and utilities. Built-in integration with `otter test`.

## Usage
```otter
use test;

~> test_math() -> void {
    test.eq(1 + 1, 2, "Math works!");
}
```
