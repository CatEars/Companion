# Kattis Submit

Submits a file to kattis with all accompanying files (header files,
imported files). Uses the kattis provided submit script to submit
files.

Below is a video showing how it the script is used. It first shows the
solution to the complicated problem `carrots`. Then it uses the submit
script and shows the result on `open.kattis.com`.

![Kattis Submit Example Usage](docs/img/submit.webm)

Example usage:

```bash
$ ls kattis/cross
cross.cpp cross.md
$ cat kattis/cross/cross.cpp | wc -l
187
$ ./script/kattis_submit cross
Submission received. Submission ID: 2398678.
$ ... Open kattis profile and check submission status ...
```
