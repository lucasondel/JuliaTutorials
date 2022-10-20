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
``
> **Note**
> To make the installation persision simply add the previous command
> to your `~/.bashrc` file.

That's it ! Now you should be able to start a sessions:
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
