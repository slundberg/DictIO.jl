# DictIO

[![Build Status](https://travis-ci.org/slundberg/DictIO.jl.svg?branch=master)](https://travis-ci.org/slundberg/DictIO.jl)

This is a simple utility designed to ease the saving and loading of dictionaries in Julia. It is designed for use cases where you want a representation of a dictionary that is easy to load, maintains types, and is easy to read with any text editor or spreadsheet.

Note that not all types are supported and a tab delimited format is used.

### Sample usage

```julia
d = Dict{ASCIIString,Int64}()
d["a"] = 1
d["b"] = 50
writedict("tmp.txt", d)
d2 = readdict("tmp.txt")
```

where `d2` is
```
Dict{ASCIIString,Int64} with 2 entries:
  "b" => 50
  "a" => 1
```

and `tmp.txt` is

```
ASCIIString Int64
b 50
a 1
```
