# Simple Shell

A small Unix-like command interpreter written in C. This educational project explores how a shell reads input, resolves commands, manages environment variables, launches child processes, and reports execution errors.

## Features

- Interactive and non-interactive execution
- Command lookup through `PATH`
- Process creation with `fork` and program execution with `execve`
- Built-in commands including `cd`, `exit`, `env`, `setenv`, `unsetenv`, `history`, and `alias`
- Command chaining with `;`, `&&`, and `||`
- Variable and alias replacement
- Persistent command history
- Script-file input

## Build

The project targets a POSIX-like environment with GCC.

```bash
git clone https://github.com/Nkosi24/simple_shell.git
cd simple_shell
gcc -Wall -Werror -Wextra -pedantic *.c -o hsh
```

## Run

Interactive mode:

```bash
./hsh
```

Non-interactive mode:

```bash
printf "pwd\nexit\n" | ./hsh
```

Run commands from a file:

```bash
./hsh commands.txt
```

## Example

```text
$ ./hsh
$ pwd
/path/to/simple_shell
$ echo Hello
Hello
$ exit
```

## Project structure

| Area | Files |
| --- | --- |
| Entry point and loop | `main.c`, `shell_loop.c` |
| Parsing and tokenization | `parser.c`, `tokenizer.c`, `getLine.c` |
| Built-ins | `builtin.c`, `builtin1.c` |
| Environment handling | `environ.c`, `getenv.c` |
| History and aliases | `history.c`, `builtin1.c` |
| Error handling | `errors.c`, `errors1.c` |
| Shared declarations | `shell.h` |

## Validation

Compile with strict warnings enabled:

```bash
gcc -Wall -Werror -Wextra -pedantic *.c -o hsh
```

## Learning focus

This project demonstrates process control, system calls, memory management, string parsing, linked lists, and environment management in C.

## Repository owner

Adede-Nkosi Essien — [GitHub](https://github.com/Nkosi24)
