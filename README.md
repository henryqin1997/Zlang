# Zlang

Trying to build a programing language which can interoperate most existing programming languages

## Target example
```
import main from cplusplus.cpp as cmain
import mypythonfile from ./mypythonfile.py
chain:block1{
  java(input: (int[], stdin), output: int):x1{
    ...(input);
    System.out.println(out);   //output=out, marshalling after this point, depening on chain structure
  },
  c++(intput: (int, x1), output: int[]):x2{
    cmain(input);
    cout<<out;
  },
  python3(intput: (ndarray<>, x2), output: (int,stdout)){
    print(mypythonfile(input));
  }
}
block3=copy(block1)
parallel:block2{
  block1;
  block3;
}
run:block2
```
Then the program run two block1 in parallel (maximizing use of cpu core), and in block1 run each part of code in order, with later one's input specified by argument, from stdin or previous output, and output to specified place (file or stdout).

## Components needed (Unfinished)
Interpreter
Marshaller
Scheduler
Linker
