# CC-Brainfuck-Interpreter

This is a Brainfuck interpreter designed to run on CraftOS, written in Lua. Brainfuck is an esoteric programming language known for its minimalism and Turing completeness.

## Overview

This interpreter allows you to execute Brainfuck programs within the CraftOS environment. It provides a command-line interface for inputting Brainfuck commands interactively or loading Brainfuck code from files.

## Features

- Interactive command-line interface
- Load Brainfuck code from files
- Visualizes the memory cells and current pointer position
- Input/output capabilities
- Reset interpreter functionality

## Usage

### Running the Interpreter

To start the Brainfuck interpreter, simply run the Lua script in CraftOS.
But you can also run .bf files directily without the visualizer and everything else. Just runs the bf code straight up and only prints the output

```shell
brainfuck <PATHTOFILE>
```

### Interactive Mode

In interactive mode, you can directly input Brainfuck commands one by one.

- `Q` or `q`: Quit the interpreter
- `R` or `r`: Reset the interpreter
- `L` or `l`: Load a Brainfuck file

### Loading a File

To load a Brainfuck file, type `L` or `l` in the interactive mode prompt, then enter the path to the file when prompted.

### Brainfuck Commands

The Brainfuck commands are as follows:

- `>`: Increment the data pointer
- `<`: Decrement the data pointer
- `+`: Increment the byte at the data pointer
- `-`: Decrement the byte at the data pointer
- `.`: Output the byte at the data pointer
- `,`: Input a byte and store it in the byte at the data pointer
- `[`: Jump forward to the command after the matching `]` if the byte at the data pointer is zero
- `]`: Jump back to the command after the matching `[` if the byte at the data pointer is nonzero

## Example

Here's a simple example of a Brainfuck program that prints "Hello, World!":

```brainfuck
>+++++++++[<++++++++>-]<.>+++++++[<++++>-]<+.+++++++..+++.>>>++++++++[<++++>-]
<.>>>++++++++++[<+++++++++>-]<---.<<<<.+++.------.--------.>>+.>++++++++++.
```

