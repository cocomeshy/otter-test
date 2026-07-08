# otter-test

Hard-exit assertions for main()-style test programs.

Part of the Otter standard library. Otter is a compiled systems language with no garbage collector and no libc dependency (pthread for threading is the one exception); everything else goes through raw syscalls and DLL imports.

## Install

In your `otter.nest`:

```nest
deps {
  use "test" want "1.0.0"
}
```

Then:

```sh
otter pkg pull
```

## API reference

### `test.assert(cond:bool, msg:str)`

Assert a condition is true. If false, prints the message and exits with code 1.

Parameters:

- `cond`: The condition to check
- `msg`: Message to print on failure

### `test.eq(got:int, want:int, msg:str)`

Assert two integers are equal. If not, prints the message and exits with code 1.

Parameters:

- `got`: The actual value
- `want`: The expected value
- `msg`: Message to print on failure

### `test.neq(a:int, b:int, msg:str)`

Assert two integers are NOT equal. If equal, prints the message and exits with code 1.

Parameters:

- `a`: First value
- `b`: Second value
- `msg`: Message to print on failure

### `test.str_eq(got:str, want:str, msg:str)`

Assert two strings are equal (byte-by-byte comparison). If not equal, prints the message and exits with code 1.

Parameters:

- `got`: The actual string
- `want`: The expected string
- `msg`: Message to print on failure

### `test.ok(msg:str)`

Print an informational message (typically test-section name on success).

Parameters:

- `msg`: Message to print

---

## Dependencies

memory, io, os.

## License

MIT.
