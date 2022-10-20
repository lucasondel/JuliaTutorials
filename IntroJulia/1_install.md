# Introduction to Julia

In brief: [The Julia Programming Language](https://julialang.org/)

## Installation

Download the archive corresponding to your system requirements here:
[https://julialang.org/downloads/](). For instance:
instance
```
$ wget https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz
```
then extract the compressed archive:
```
$ tar xvf julia-1.8.2-linux-x86_64.tar.gz
```
and finally update your path:
```
$ export PATH="$PWD/julia-1.8.2/bin:$PATH"
```
> **Note**
> To make the installation persitent simply add the previous command
> to your `~/.bashrc` file.

That's it ! Now you should be able to start a session:
```
$ julia
               _
   _       _ _(_)_     |  Documentation: https://docs.julialang.org
  (_)     | (_) (_)    |
   _ _   _| |_  __ _   |  Type "?" for help, "]?" for Pkg help.
  | | | | | | |/ _` |  |
  | | |_| | | | (_| |  |  Version 1.8.2 (2022-09-29)
 _/ |\__'_|_|_|\__'_|  |  Official https://julialang.org/ release
|__/                   |

julia>
```

## Julia REPL
Julia provides a interactive command-line (REPL for "read-eval-print-loop") which is started by typing `julia`. 
The REPL has 3 running mode: 
* `julia` mode (default) which allow to run julia statement
* `pkg` (accessible by typing `]`) to manage dependencies
* `shell` (accessible by typing `;`) to issue standard shell commands.

## Managing dependencies
To install a new package, say [LogExpFunctions](https://github.com/JuliaStats/LogExpFunctions.jl) open the julia 
REPL, enter the `pkg` mode and type:
```
pkg> add LogExpFunctions 
```
You can check the packages you have installed by typing:
```
pkg> status 
[2ab3a3ac] LogExpFunctions v0.3.18
```
To remove a package type:
```
pkg> rm LogExpFunctions
```
> **Note**
> The environment variable `JULIA_DEPOT_PATH` controls where will be installed the julia packages. See [https://docs.julialang.org/en/v1/manual/environment-variables]() for the list of environment variables used by julia.

## Virtual environments

Julia has built in tools to create manage Virtual Environments (VE). Each VE is associated to a directory so the first step is to create a new folder:
```
$ mkdir myproject
$ cd myproject
```
Inside `myproject` directory open a julia REPL and in `pkg` mode type:
```
pkg> activate .
```
> **Note**
> Actually, it is not necessary to be in the directory to use the VE, instead you can activate any path you want:
> ```
> pkg> activate /path/to/my/virtual/env
> ```

You can the add and remove your dependencies using the `add` and `rm` command as usual.

## Creating a package 

See: [https://pkgdocs.julialang.org/v1/creating-packages/]()
