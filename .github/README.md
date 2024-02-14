# ARM ![](https://img.shields.io/badge/an_ARM_project-darkgreen) ![GitHub License](https://img.shields.io/github/license/armlang/arm) ![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/armlang/arm)
ARM is a free, open-source, basic programming language inspired by Python and C++. At it's core is an easy-to-modify interpreter that works with any 
Bash (Linux / Mac OS X) or DOS system.

## What does it look like?
```rs
import c
import "thismodule.arm" as MyModule

/*
import works as: import(file, reference). The reference is how you call functions from it.
For example, if you import "thismodule.arm" as "ThisModule" and include a function called run() inside of thismodule.arm,
You run it from your code by running ThisModule.run().
*/

fn main() {
  print("Hello world!")

  if 1 > 1 {
    print("that's not true, something is wrong)
  } else {
    print("hooray")
  }

  c.run(ifn() {
    /*
    ifn is an easy way to include code inside of an execution block.
    In this example, ifn (inline function) is used to execute any C code inside of it's block.
    */

    #include <iostream>

    void main() {
      printf("Hello world!");
    }
  })

  var MyVar = 1
  /*
  var is an auto-declaration keyword, but you can limit it's values by explicatly declaring a type.
  Do this with this example:

  var MyVar: integer = 1;

  You can also limit it's values with another argument.

  var MyVar: {integer, 1, 99} = 1;

  It's value is locked to numbers inbetween 1 and 99.
  */
}
```

## Roadmap
- [X] Development launch
- [ ] Basic interpreter (runnable via command line ``arm cli``)
- [ ] .arm file interpreter
- [ ] GitHub / GitLab and other progress bar support

## Looking to issue pull requests?
Currently, ARM does not check pull requests as the development is still in very early progress. As the language becomes more detailed, ARM will begin to accept pull requests via [GitHub](https://github.com/armlang/arm).
