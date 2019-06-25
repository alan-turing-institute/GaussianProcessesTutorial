# Gaussian processes with Julia
**authors**: Oliver (ostrickson@turing.ac.uk) & Mohamed Ali (mal-badri@turing.ac.uk)

An introduction to Gaussian processes and Julia -- we explore Gaussian
processes by implementing them in Julia.

The requirements are 
- Julia (https://julialang.org/downloads/).  It has been tested with Julia v1.1.
- IJulia (the Julia Jupyter kernel, https://github.com/JuliaLang/IJulia.jl).  To install it, run
```
$ julia
julia> Pkg.add("IJulia")
julia> quit()
```

Launch the notebook

```
$ jupyter notebook gp.ipynb
```

The notebook will try to install a few additional Julia packages itself.

## Troubleshooting

If you get an error such as
```
IOError: [Errno 13] Permission denied: u'/Users/user/.jupyter/migrated'
============================================[ ERROR: IJulia ]=============================================

LoadError: failed process: Process(`/Users/user/.julia/v0.6/Conda/deps/usr/bin/jupyter-kernelspec install --replace --user /var/folders/zx/j_gjm0ld081b_mcqmg3gp9l1zp59y6/T/julia-0.6`, ProcessExited(1)) [1]
```
verify who owns the directory `~/.jupyter` with `ls -la ~/.jupyter`. If `root` owns it, change ownership with 
```
sudo chown user: ~/.jupyter/
```
replacing `user` with your username. IJulia will already be installed, so you'll need to remove IJulia and start over, or install Jupyter separately with instructions [here](https://jupyter.org/install).
