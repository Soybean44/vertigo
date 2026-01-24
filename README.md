# Vertigo

## Description

This project is a compiler for my esoteric language vertigo. This language is not meant to be usable it's just a fun project to see if I can parse and compile a language like this. What is the language you may be asking? Well let me show you how to write hello world

```
"p
hr
ei
ln
lt
o;

w
o
r
l
d
!
"
;
```

Yes it's that painful.
For more information, read Docs.md
# Usage

To compile a vertigo file, run the following command:

```
vertc <input_file>.vert <output>
```
This will compile the vertigo file into a bytecode file that can be run on the vertigo virtual machine. As by convention the output file should have the extension `.vte` standing for vertigo executable.

To run the compiled bytecode file, use the following command:

```
vertigo <program>
```

When developing, you can also run the individual binaries directly from cargo using:

```
cargo run --bin vertc <input_file>.vert <output> 
cargo run --bin vertigo <program>
```

