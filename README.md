[![Build Status](https://travis-ci.org/bast/pybind11-demo.svg?branch=master)](https://travis-ci.org/bast/pybind11-demo/builds)
[![License](https://img.shields.io/badge/license-%20MPL--v2.0-blue.svg)](../master/LICENSE)


# pybind11 demo

Demonstrates how to call a C++ class from Python using pybind11 and VS 2017


## How to build this demo

In x64 Native tool command prompt for visual studio 2017:

```
git clone --recursive https://github.com/bast/pybind11-demo.git
cd pybind11-demo
mkdir build
cd build
cmake -A x64 ..
devenv /build Debug example.sln
```


## Example test run

```python
>>> from example import add
>>> add(2, 3)
5
>>> from example import Pet
>>> my_dog = Pet('Pluto', 5)
>>> my_dog.get_name()
'Pluto'
>>> my_dog.get_hunger()
5
>>> my_dog.go_for_a_walk()
>>> my_dog.get_hunger()
6
```
