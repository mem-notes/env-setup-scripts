**Python comes preinstalled on almost every Linux system** but it may not using `python` as execute command

A simple safe way would be to use an alias. Place this into ~/.bashrc or 
~/.bash_aliases file:

```shell
alias python=python3
After adding the above in the file, run source ~/.bashrc or source ~/.bash_aliases.
```
For example:
```shell
$ python --version
Python 2.7.6
$ python3 --version
Python 3.4.3
$ alias python=python3
$ python --version
Python 3.4.3
```