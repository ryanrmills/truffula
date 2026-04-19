# Truffula Notes
As part of Wave 0, please fill out notes for each of the below files. They are in the order I recommend you go through them. A few bullet points for each file is enough. You don't need to have a perfect understanding of everything, but you should work to gain an idea of how the project is structured and what you'll need to implement. Note that there are programming techniques used here that we have not covered in class! You will need to do some light research around things like enums and and `java.io.File`.

PLEASE MAKE FREQUENT COMMITS AS YOU FILL OUT THIS FILE.

## App.java
- Main entry point for the program.
- Will build a `TruffulaOptions` from CLI args.
- Will create `TruffulaPrinter` and call `printTree()`.

## ConsoleColor.java
- Enum of ANSI color codes used for terminal output.
- Each enum value stores its escape code string.
- `toString()`/`getCode()` return the code for printing.

## ColorPrinter.java / ColorPrinterTest.java
- `ColorPrinter` wraps a `PrintStream` and prints with the current `ConsoleColor`.
- `print`/`println` support optional color reset after writing.
- Test checks exact output format (color code + message + newline + reset).

## TruffulaOptions.java / TruffulaOptionsTest.java
- Stores parsed options: root directory, show hidden, and use color.
- CLI constructor (`String[] args`) is TODO and must validate flags/path.
- Test verifies valid args set root correctly, enable hidden, and disable color.

## TruffulaPrinter.java / TruffulaPrinterTest.java
- `TruffulaPrinter` is responsible for recursive tree printing.
- `printTree()` is TODO; should handle indentation, sorting, hidden filtering, and color levels.
- Test builds a real folder tree and asserts exact printed output including colors/order.

## AlphabeticalFileSorter.java
- Helper utility with static `sort(File[])`.
- Sorts by filename ignoring case via lambda comparator.
- Intended for consistent tree output ordering.
