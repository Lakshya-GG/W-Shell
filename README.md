# W-Shell

W-Shell is a user-friendly yet powerful command-line shell designed for Unix-based systems. It offers users the ability to execute commands, handle file redirection, utilize pipes, chain commands, and access a history of previously executed commands.

## Features

- **Command Execution**: Run standard Unix commands.
- **File Redirection**: Supports input (`<`), output (`>` and `>>`) redirection.
- **Pipes**: Allows command chaining using pipes (`|`).
- **Command Chaining**: Supports chaining commands with `;`, `&&`, and `||`.
- **Command History**: Navigate through the history of executed commands with custom history management.

## Getting Started

To use W-Shell, compile the project using a C compiler such as `gcc`. Follow these steps:

1. Clone this repository or download the source code.
2. Navigate to the directory containing the source code.
3. Compile the code using this command:

```bash
make
```

4. Start the shell:

```bash
./wshell
```

You can also execute commands from a file by providing the filename as an argument:

```bash
./wshell filename.txt
```

## Internal Commands

W-Shell includes several built-in commands:

- `cd`: Change the current directory.
- `clear`: Clear the terminal screen.
- `hist`: Access the command history. Use `u` (up) and `d` (down) to navigate, `y` to execute a command from history, and `q` to exit history mode.
- `exit`: Exit the shell.

## File Structure

- `main.c`: The main entry point of the shell, containing the primary loop for command execution.
- `parse.c`: Contains the logic for parsing command line input into tokens.
- `pipe.c`: Manages command piping (`|`).
- `redir.c`: Handles file redirection (`<`, `>`, `>>`).
- `history.c`: Implements the command history feature.
- `exe.c`: Executes commands, including internal commands, redirection, pipes, and chaining.
- `env.c`: Substitutes environment variables with their values in commands.
- `chain.c`: Manages command chaining (`;`, `&&`, `||`).
- `header.h`: The header file with necessary includes and function declarations.

## Contributions

Contributions to W-Shell are welcome! Feel free to fork the repository, make changes, and submit pull requests.
```