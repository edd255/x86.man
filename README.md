# x86-manpages

Clone this repository, add the directory `manx86` to `MANPATH`, and `x86` to `MANSECT`.
Now, you can access the manpages via `man x86 <instruction>`.

## Methodology

Man pages are generated from Intel's official documentation like:

PDF --> html --> markdown --> man page

Conversion to html of Intel's PDF documentation is made by [Félix Cloutier](https://www.felixcloutier.com/x86/index.html); which was most of the work.

Other steps are performed in this project; with help of various tools. See "scripts" directory.


## Contribution

Maintainer gave up fixing bug-producing scripts, after he found out most of them could be ignored and perfection was not the goal. If you cannot ignore an imperfection you saw, please consider adding necessary fix to the bash scripts by a PR. Or if you know "troff", you can directly fix outputs (in "manpages" directory) by sending a PR.

### Bugs

Since scriptized, unhandled exceptions exist. Most of them related to tables; especially `rowspan`s. Nowadays, `rowspan-normalizer` script is missing th and tr rowspan normalizer functions. And also `[` and `]` and some other characters break tables; probably they must be escaped while the doc was still in the html form.

## License

See LICENSE file, which is for the scripts used to generate the man pages. `Copyleft` sign in the ready-to-use outputs in this repo does not claim any rights on the Intel's original documentation; and just stands for the conversion process made, and more than this, just for fun.
