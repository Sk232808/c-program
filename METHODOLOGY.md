# Methodology

## 1. Take Input

The web page displays five input boxes. Each box accepts the marks for one subject, from `0` to `100`.

## 2. Send The Form

When the user clicks **Check result**, the browser sends the five values to the C server using an HTTP `POST` request.

## 3. Validate The Marks

The C program reads each submitted value and checks that:

- All five values are present.
- Every value is a valid number.
- Every value is between `0` and `100`.

If any check fails, the program displays an error message.

## 4. Calculate The Average

The program adds the five marks and divides the total by five:

```text
percentage = total marks / 5
```

Because every subject is marked out of `100`, this average is also the overall percentage.

## 5. Decide The Result

The program compares the percentage with `33`:

```text
if percentage >= 33
    show pass message
else
    show fail message
```

A percentage of exactly `33%` is treated as a pass.

## 6. Send The Result To The Browser

The C server creates an HTML response. The browser displays the average percentage and either:

- `Congratulations! You passed.`
- `You failed.`

## Technologies Used

- C programming language
- Windows Winsock for networking
- HTML and CSS embedded in the C source
- HTTP `GET` and `POST` requests
