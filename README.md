# Companion

Kattis is a great judge. However, Kattis is not your best
friend. Kattis can be a bit harsh at times, killing your (hopefully)
well designed programs prematurely. Sometimes Kattis can seem a bit
cold, but we know that in reality she has a heart of silicon (better
than gold). Kattis will be there for you in your ups and downs and
that is what we call a true Companion.

This repository has a bunch of tools that help you in using
Kattis. The tooling is aimed at being very simple to use and beginner
friendly. You can see usage examples inside the `docs/` folder to get
a better understanding of how it all works.

# Setup

The scripts are pretty self-contained. They use python and mostly
operate on the filesystem and do some network calls. You have to
download your kattis token if you want to submit directly to kattis
however. You can follow
[this guide](https://open.kattis.com/help/submit) to help you download
your personal configuration file. The above one goes to
`open.kattis.com` so if you are using a local kattis, like
`liu.kattis.com`, then you will need to go into the help pages and
find it on that site.

The submit script uses `requests` to submit so you will need to
install this by running `sudo -H pip install requests`.

# Contributing

Since this is open source and I do not have an infinite amount of time
on my hands I would very much appreciate contributions and
ideas. Please use pull requests for this and send an email to me at
`anting004@gmail.com`. I do not use github that much so a lonely PR
might go unanswered for a long time.

## Appreciated Contributions

Here are some extra appreciated contributions/features that would be
useful.

### Tab Completion

I am currently investigating how we can use tab completion in scripts
like `kattis_test` and `kattis_submit`. What I am looking at would
only work in bash (which is the shell I use). If you know how it works
for other shells or have a solution that works for "all" shells it
would be greatly appreciated.

### Remove Dependency on Requests

Even tough `requests` is an awesome library it is the only library not
from the python standard library that is used. It is used by the
submit.py script supplied by Kattis. The submit script uses two parts,
the request.post method and exceptions so it should be really easy to
replace. This would be a very welcome contribution.

### Additional Scripts

I would also like to have two more scripts.

One that looks at "the last submitted problem" as well as allows you
to specify a submission ID or a problem ID and tells the user if it
got accepted or not, preferably showing how many test cases it got and
if it failed, what happened. (e.g. AC, WA, TLE, MLE etc.). Could call
this something like `kattis_last`.

The second would be a script running for a bit of a longer time
downloading all solutions available and putting them into their
appropriate folders. For example if I have solved `carrots` and
`hello` it should download my most recent accepted solutions to those
problems and put the files into `kattis/carrots` and
`kattis/hello`. Would be called somethine like `kattis_download`.

The biggest problem with the above two scripts is that I would like to
use standard library python as far as possible. Currently the only
thing you have to do is get a token from kattis, but I do not want it
to be much more than that. Both of the above would be super simple to
solve with Beautiful Soup but I do not want users to have to
(eventually) fight with installing that for scripts that are not
necessary. If you can do the above with something like
`xml.etree.ElementTree` it would be greatly appreciated tough.

### Windows

I do not use Windows for programming but if these scripts would work
on Windows as well then that would be cool. Not sure how useful people
would find it tough.

### Java

I think that the most common languages for competitive programming is
C++, Java and python (I believe) and since this repo works with C++
and python already it only misses Java support. If someone wants to
add Java support then that would be appreciated.

## Non-appreciated Contributions

These are contributions that would be ignored or removed.

* Github Issues. I don't use github that much. Send me an email at
  `anting004@gmail.com` if you have an issue you want to report. If
  you have a bug fix, please create a PR and mail me.

* PRs With Big Structural Changes. The repo is designed around
  simplicity. Problems go into `kattis`, library code goes into
  `library`, tests go into `tests`. It allows an experienced user to
  have close to no friction in starting, documenting, testing and
  submitting solutions. Optimizing this process will have minimal gain
  for anyone involved. Adding too many features will reduce simplicity
  and create a barrier to entry. If you want the best tool for the job
  you are free to fork this and do what you want with it but I have no
  use for large, breaking, changes and neither do those that I want to
  attract with this repo.

* Things you would typically find in an algorithm library. Users are
  free to download whatever they want into the `library`. Preferably
  they create something that is useful to them over time and if your
  algorithm implementation is useful then they might choose to use
  that but I will not put it in this repo.

* Tests for kattis problems. An important part of learning how to
  program competitively is to discover how to debug correctly. Tests
  in kattis often omit edge-cases to teach a lesson. That the
  edge-cases of a problem will need to be thought about during the
  whole process. They are omitted for the benefit of the
  programmer. They are only useful when you have struggled with a
  problem, not upfront.

* Solutions to kattis problems. No.. Just no...
