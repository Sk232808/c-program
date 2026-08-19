# Five-Subject Marks Result Checker

A simple web application written in the C programming language.

## Live Demo

[Open the Marks Result Checker](https://beamish-cendol-3ade7d.netlify.app)

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

## Methodology

1. The web page displays five input boxes for subject marks from `0` to `100`.
2. The browser sends the submitted values to the C server using an HTTP `POST` request.
3. The C program checks that all five values are present, numeric, and within the valid range.
4. The program adds the five marks and divides the total by five. Because each subject is out of `100`, this average is the overall percentage.
5. The program compares the percentage with `33`. A percentage of exactly `33%` is a pass.
6. The C server sends an HTML response showing the average and the pass or fail message.

```text
if percentage >= 33
	show "Congratulations! You passed."
else
	show "You failed."
```

## Technologies Used

- C programming language
- Windows Winsock for networking
- HTML and CSS embedded in the C source
- HTTP `GET` and `POST` requests

## Files

- `shivam.c` - C web server and marks calculation logic.

## License

This project is available for learning and personal use.
