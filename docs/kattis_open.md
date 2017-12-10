# Kattis open

This scripts opens a new problem and copies your template to the
problem directory and creates a markdown file where you can enter your
solution idea. It also creates the tests directory if not present and
fetches sample input from kattis.

Entering a solution idea is very useful if you ever come back to the
problem and want to study it later. It is also useful in case you want
to present your solution to someone else but most importantly you will
spend less total time on the problem by finding the solution before
writing it.

Below is an example use of the script. At first the folder does not
exist. When the script is run it creates copies a template to the
folder and creates a markdown file. We can also see that the sample
data was downloaded.

![Kattis Open running example](./img/open.webm)

This script can also take a third argument, which can be either `cpp`
or `py` and copy the corresponding template into the opened problem.

For example `kattis_open carrots py` would move `library/template.py`
into the `kattis/carrots` folder instead of `library/template.cpp`.

Example usage:

```bash
$ ./scripts/kattis_open happyprime
'happyprime' was successfully opened, time to get solving!
Samples fetched from kattis and put into tests folder
$ ls kattis/happyprime
happyprime.cpp  happyprime.md
$ ls tests | grep happyprime
happyprime
$ ls tests/happyprime
sample.ans  sample.in
```

