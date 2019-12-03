# python-sasl

Python wrapper for Cyrus SASL

## how `sasl3` is different from `sasl` package? 

This is a fork from original work from Cloudera's package [sasl](https://github.com/cloudera/python-sasl) package. 

Original package wasn't maintained and had issue wth latest Python 3 releases, and also had runtime issues running 
on RHEL6. Python `sasl3` package solves these issues.

Other than that, it's a drop-in replacement for original `sasl` package - no changes to your Python code is necessary, 
including the name of the imported package - still stays just `sasl` (and not `sasl3` as the name of the pypi repo). 

## External dependencies

You need following external packages installed on the system to pip-install `sasl3` :
- C compiler (e.g. `gcc`)
- `cyrus-sasl-devel` package for Cyrus header files.

Both can be installed with OS' package manager, e.g. 
```bash
yum install gcc cyrus-sasl-devel.x86_64

```

## to generate sasl/saslwrapper.cpp from the pyx file:

run `./recython.sh`
