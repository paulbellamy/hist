# hist
### Pipe-able Command-line Histograms

Because sometimes you want to take a bunch of numbers and compute a histogram. Works great with [spark](https://github.com/holman/spark)

## Install

hist is an executable ruby script, so drop it somewhere in your `$PATH`.

## Requirements

* Ruby

## Usage

```
$ hist -h
USAGE: hist [OPTION]... FILE...
Computes a histogram from unsorted numbers (one-per-line) from FILES (or standard input)
and writing to standard out. The min and max are taken from the data.

Input reads the first number per line, and results are printed one bucket per
line, in the format:
<count> <bucket lower bound>

OPTIONS:
  -h, --help         Show Help Message
  -b, --bucket-size  Bucket Size (default 100)

EXAMPLE:
  $ echo "1\n100\n110\n200" | hist -b 100
  1 0
  2 100
  1 200
```
