# Kattis Compile

This script will compile your program (if it is a compiled language)
and then put it inside the "compiled" folder. If it is in interpreted
language then it will move all parts of the program to the "compiled"
folder and you can run them from there.

This script is mainly used for debugging single programs.

In the webm you can see a sample use case where the problem
`kastenlauf` is compiled and then run manually.

![Kattis Compile running example](docs/img/compile.webm)

C++ example usage:

```bash
$ ./scripts/kattis_compile almostunionfind
run ./compiled/almostunionfind to run the program
$ ./compiled/almostunionfind < tests/almostunionfind/sample-1.in
...
```

Python example usage:

```bash
$ ./scripts/kattis_compile rafting
copied files to compiled/ run "python compiled/rafting.py" to run the program
$ python compiled/rafting.py < tests/rafting/sample-1.in
```

