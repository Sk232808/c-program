# Five-Subject Marks Result Checker

A simple web application written in the C programming language.

Enter marks for five subjects, and the app calculates the average percentage:

- `33%` or more: **Congratulations! You passed.**
- Less than `33%`: **You failed.**

The application accepts marks from `0` to `100` for each subject.

## Project Description

This project demonstrates how a C program can act as a small web server. It uses Windows Winsock to receive browser requests and sends back an HTML page containing the marks form and result.

## Requirements

- Windows
- MSYS2 with the UCRT64 GCC compiler
- A web browser

## Build And Run

Open the **MSYS2 UCRT64** terminal and run:

```bash
cd "/c/Users/shiva/c-program-publish"
gcc shivam.c -o shivam.exe -lws2_32
./shivam.exe
```

Open this address in your browser:

```text
http://127.0.0.1:8080
```

Press `Ctrl+C` in the terminal to stop the server.

## How The Result Is Calculated

The program adds the five marks and divides the total by five:

```text
average percentage = (mark 1 + mark 2 + mark 3 + mark 4 + mark 5) / 5
```

For example, marks of `40, 50, 60, 70, 80` produce an average percentage of `60%`, so the result is pass.

## Validation

The app shows an error when:

- A subject mark is missing.
- A mark is less than `0`.
- A mark is greater than `100`.

## Files

- `shivam.c` - C web server and marks calculation logic.
- `METHODOLOGY.md` - Simple explanation of how the application works.

## License

This project is available for learning and personal use.
