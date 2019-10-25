# Systems Research
- Systems research: solving problems in computer systems
	- Performance, energy consumption, cost, security, etc.
- Worst research: try to solve non-existing problems
	- *Make the performance of a keyboard device driver 10x faster*
	- *Does the performance of the keyboard device driver really
      matter?*
- **Finding real, important problems are critical**

# How to find *real, important problem*
- Read recent conference/workshop papers
	- What problem area is important
	- What problems are already solved and what are not solved yet
	- What are commonly used techniques in this field
	- What are commonly agreed ways to evaluate a proposed methodology
- However, a paper is the result of at least one-year effort
	- *You are already two years behind than the authors*

# How to find real, important problem *as early as possible*
- Attend top-tier conference and *chat with researchers*
	- *What are you working on these days?*
	- Good to get a sense of research direction
	- If you are lucky, you can find a new, interesting problem
- Build a prototype of an existing system
	- Best way to have deepest understanding of an existing system
	- It takes time so it is risky if there is no new, interesting problem
- Benchmarking
	- Economic way to find new, important problems

# How to use benchmarking to *discover new problems*
- Run existing benchmark in new setting
	- E.g., run `mosbench` on 200 core machine
	  -> *Can we find any new bottleneck?*
	- E.g., run `mosbench` on docker, virtual machine, or unikernel
	  -> *Does new isolation mechanism introduce new overhead?*
	- E.g., run `FxMark` on an extremely-fast NVM or a slow SMR drive
	  -> *How does performance characteristics of storage device
	  affect performance and scalability of storage stack?*

# How to use benchmarking to discover new problems
- Compare existing approaches with the same benchmark
	- Can have deeper understanding of existing approaches
	  beyond what described in the paper
	- *Can draw design principles of a new approach*

# What are important in benchmarking
- **This is not an one time job**
	- Automation, automation, automation!
- **Without automation, this is not a reproducible science.**
	- We human do make mistakes.
	- Automation is one of way to avoid mistakes (or make the same
      mistakes consistently)
- **If we are copying log files here and there,
    this is the sign that we should automate**

# What are important in benchmarking
- **Automate as much as possible**
	- Run all necessary combinations of experiments
	- Generate graphs
	- (Email generated graphs automatically)
- **It does affect our productivity a lot!**
	- Run a benchmark script before having meeting (or going to bed,
      leaving office, etc)
	- After meeting, check graph and devise what to run next or what
      to profile
- **`bash`, `awk`, and `python` are our friends**

# Examples of good benchmarks
- `Mosbench` (or our forked `vbench`)
	- https://pdos.csail.mit.edu/archive/mosbench/
	- https://github.com/sslab-gatech/vbench
- `FxMark`
	- https://github.com/sslab-gatech/fxmark

# Tips for more meaningful benchmarking
- Make your results easy to compare
	- `# transactions/msec` instead of `# transactions`
	- `Abort ratio` instead of `# aborts`
- Double check benchmark parameters
	- number of initial elements in a hash table
	- update ratio
	- random distribution: uniform vs. zipf

# Tips for more meaningful benchmarking
- Know your hardware
	- Take care of CPU topology in pinning threads
	- Check `/proc/cpuinfo`
	- Or use
      [cpu-topology.py](https://github.com/ssrg-vt/os-scalability-benchmark/blob/master/tools/cpu-topology.py),
      [cpu-sequences](https://github.com/ssrg-vt/os-scalability-benchmark/blob/master/vbench/support/cpu-sequences),
      or [set-cpus](https://github.com/ssrg-vt/os-scalability-benchmark/blob/master/vbench/support/set-cpus)
- Avoid well-known bottlenecks
	- Use scalable memory allocator, such as `jemalloc` or `tcmalloc`
- Use `git`, `tmux`, and `gnuplot`, seriously
