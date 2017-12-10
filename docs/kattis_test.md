# Kattis test

Tests the problem against input available in the tests
directory. Provides instant feedback with what went wrong or if the
program works on all specified input. The file searches for pairs of
`X.in` and `X.ans` and compares these two. If you have complex output
then this can be decieving.

The testscript looks at the first line of input to determine what type
of python is used, this means that you need to include the string
'python3' in the first line (for example a shebang), else it will use
python2 to run it.

```bash
$ ls kattis/busnumbers
busnumbers.cpp busnumbers.md
$ cat kattis/busnumbers/busnumbers.cpp | wc -l
51
$ ls tests/busnumbers
mine-1.ans  mine-1.in  sample-1.ans  sample-1.in
$ ./scripts/kattis_test busnumbers
===> sample-1.in
1c1
< 141-144 174 175 180
---
> 141-143 174 175 180
$ edit kattis/busnumbers/busnumbers.cpp
    ...
$ ./scripts/kattis_test busnumbers
✔ - AC
```
