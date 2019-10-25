# Useful Linux Tools

## Version control: `git`
- [Atlassian tutorial](https://www.atlassian.com/git/tutorials)
- [Github tutorial](https://try.github.io/)
- [Tutorials point](https://www.tutorialspoint.com/git/index.htm)
- [bash-git-prompt](https://github.com/magicmonty/bash-git-prompt):
  informative bash prompt for git

## Source code browsing
- [cscope](https://courses.cs.washington.edu/courses/cse451/12sp/tutorials/tutorial_cscope.html)
- [ctags](https://courses.cs.washington.edu/courses/cse451/10au/tutorials/tutorial_ctags.html)

## Tmux
- [A tmux Primer](https://danielmiessler.com/study/tmux/)

```
- tmux: start a new tmux session
- Ctrl-b %: split a pane vertically
- Ctrl-b ": split a pane horizontally
- Ctrl-b o: move to the next pane
- Ctrl-b z: zoom (or unzoom) a pane
- Ctrl-b c: create a new window
- Ctrl-b N: go to window N (0~9)
- Ctrl-b d: detach from a session
- tmux a: attach to an existing session
```

## Debugging: `gdb`
- [Cheat sheet](https://cs.brown.edu/courses/cs033/docs/guides/gdb.pdf)
- [Source level debugging](https://sourceware.org/gdb/onlinedocs/gdb/TUI-Commands.html)

```{.sh}
$> make
$> gdb --args ./unit_tests "[parser]" # run gdb for a command
gdb> b parser.cpp:100             # set a breakpoint at Line 100 in parser.cpp
gdb> run                          # actually run ./unit_tests
gdb> layout src                   # When the break point hits,
                                  # press Ctrl-x Ctrl-a to see the source code
gdb> n                            # next
gdb> s                            # step into
gdb> p VAR                        # print VAR
gdb> p *ADDR                      # print the contents at ADDR
gdb> quit                         # quit
```

## `struct` padding: `pahole`
- [The Lost Art of C Structure Packing](http://www.catb.org/esr/structure-packing/)
- [Poke-a-hole and friends](https://lwn.net/Articles/335942/)

## Performance profiling: `perf` and `ftrace`
- [Andy's performance profiling tips](https://youtu.be/unJcuufh--g?list=PLSE8ODhjZXjYplQRUlrgQKwIAV3es0U6t&t=3290)
- [perf](http://www.brendangregg.com/perf.html)
	- [Video 1](https://www.youtube.com/watch?v=FJW8nGV4jxY), [Video 2](https://www.youtube.com/watch?v=zrr2nUln9Kk)
- [ftrace](https://github.com/brendangregg/perf-tools)
- [FlameGraph](https://www.usenix.org/conference/atc17/program/presentation/gregg-flame)
- [gprof](https://sourceware.org/binutils/docs/gprof/)
	- [quick start](https://web.eecs.umich.edu/~sugih/pointers/gprof_quick.html)
	- [gprof2graph](https://github.com/jrfonseca/gprof2dot)

## Documentation: markdown
- [markdown-it demo](https://markdown-it.github.io/)
- [Markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
- [Academic Writing in Markdown](https://www.youtube.com/watch?v=hpAJMSS8pvs)
- [typora](https://typora.io/): a markdown editor and reader
- [MindForger](https://www.mindforger.com/): a markdown ide
- [Turndown](https://github.com/domchristie/turndown): an HTML to markdown converter

## Documentation
- [Installing Times New Roman for Fedora](http://mscorefonts2.sourceforge.net/)

## Graph: gnuplot or matplotlib
- [gnuplot](http://www.gnuplot.info/)
- [matplotlib](https://matplotlib.org/)


## Better terminal environment
- [tilix](https://gnunn1.github.io/tilix-web/): simple a better tiling
  terminal than gnome-terminal
- [mosh](https://mosh.org/): a better replacement of ssh
- [hack-fonts](https://github.com/source-foundry/Hack): beautiful
  fixed-width font for source code

