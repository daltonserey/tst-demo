# tst demo

> This repository is meant to contain a set of
> [tst](https://github.com/daltonserey/tst) demonstration
> activities.

To use this repository, install
[`tst`](https://github.com/daltonserey/tst), then run the command
`tst checkout <name>` (the _name_ of each activity can be found
between parentheses in the list of activities below). This will
download the files of the named activity into a directory. A
student is supposed to answer the exercise and run the automated
tests using `tst` within that directory. Teachers on the other
hand are supposed to use the directory to collect all student
answers and test them all together.

## _Hello, World!_

The `hello` activity is a good starting point to understand
`tst`, both for both students and teachers. Despite being the
simplest possible exercise in virtually any programming language,
it is an excellent case to show how `tst` tests are written and
how they are work. The activity directory includes 
7 testcases (see the file `public_tests.yaml`) as well as
6 false but
plausible answers to the exercise (the files named `answer*.py`
that are included in the activity directory).

To experiment this activity as a teacher, follow these steps:

1. install `tst`: use `pip install tst` (you may want to use a
virtual environment to experiment without using your account
environment);

2. download the `hello` activity: use `tst checkout hello hello`;
this will prompt you to choose a directory name (if you type
_Enter_ `tst` will use `hello`); then it will download the files
and save them in the directory;

3. cd into the directory; you may want to check the files; go
ahead, all files are text files; usually, both setup
and tests files use `.yaml` extension (because they are written
using _Yaml_;

4. run `tst` (without any argument); running `tst` will run all
tests in all candidate answers found in the current directory; by
default, `tst` assumes that all `.py` files are candidate answers
(this can be configured and any other programming language can be
used as well);

When you run `tst` it will print a report about the tests
executed. Because the directory contains multiple answers, `tst`
prints a report containing one line per file. Each line contains
the answer file name and a summary of the tests executed that has
one character per test. All successful tests are shown as a dot
`.` in the summary, and tests that resulted in errors or fails
are summarized with a different character (`F` is the usual
character for _fails_ and `E` for _errors_). Below you can see
the listing that is produced when you run `tst` within the
`hello` directory.

```
answer1.py .......        
answer2.py F......         
answer3.py FFF.F..         
answer4.py FFF....         
answer5.py FFFFF..         
answer6.py FFFFFF.
```

Of courde, students should receive the test files but no answer
files. To write their solution, the student must create a new
answer file and run `tst` (if the student himself has multiple
answers, it might be useful to run `tst <file>` to run the tests
exclusively on that particular file. When `tst` has a single file
under test, it prints a _debug_ style report that can be helpful
to evolve the answer.

## Activities available

- [Hello, World!](hello/hello.md) (`hello`)
- [Celsius, Fahrenheit](conversions/conversions.md) (`conversions`)
