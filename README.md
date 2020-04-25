# Zlang

Trying to build a programing language which can interoperate most existing programming languages

## Target example
import mypythonfile from ./mypythonfile.py
chain{
  java(input: int[], output: int){
    ...(input);
    System.out.println(out);   //output=out, marshalling after this point, depening on chain structure
  },
  c++(intput: int, output: int[]){
    ...(input);
    cout<<out;
  }
  python3(intput: ndarray<>, output: int){
    print(mypythonfile(input));
  }
}
