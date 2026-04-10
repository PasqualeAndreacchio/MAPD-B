## Threading and Parallel processing module

The scripts of this course module will be executed in class to demonstrate and discuss the basics of multithreading and parallel processing in Python.

The `threading` and `multiprocessing` standard Python modules will be used.

To illustrate the effect of Python Global Interpreter Lock (GIL) and its changes, a recent (`>= 3.13`) and possibly also an older (`<=3.9`) Python versions may be used.

To install older Python versions on a Debian-like Linux OS (e.g. Ubuntu), once can use the `deadsnakes` software repository:
```bash
# include a remote repository for older python versions
sudo add-apt-repository ppa:deadsnakes/ppa;
# update the list of packages
sudo apt update;
# install a specific python version (e.g. 3.7)
sudo apt install python3.7
```

Alternatively, `docker`, `venv`, or `conda` can be used to set up .

The impact of threading and multiprocessing on the CPU resources will be monitored in class using `htop` (cross-platform interactive process viewer availabe by default in Ubuntu). Any alternative CPU monitoring tool may be used 

![](pics/image.png)

The `taskset` Unix command can be used to set the affinity of a task to a given CPU or range of CPUs, to pin threads or processes to one or more CPU cores.
```bash
# execute on CPU 4 only
taskset -c 4 python3 python_script.py
# execute on CPUs 1 and 3 only
taskset -c 1,3 python3 python_script.py
# execute on CPUs from 0 to 4 only
taskset -c 0-4 python3 python_script.py
```

### Pre-requisites

1. Clone this repo (or fetch the latest updates) 
2. Have a working environment with one or more Python3 interpreters
