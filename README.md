# Random FASTA Generator

A simple application to generate FASTA files with random content based on a provided total of sequences, length of sequences and distribution of the units in the sequences.

## Compiling

You need a compiler capable of compiling C source-code written in at least the C89 standard. For GCC, the compilation can be done with the command `gcc main.c -o randomfasta`.

## Usage

Execute the application `randomfasta` to see the usage manual.

```
randomfasta (Random FASTA generator) version YYYY.MM.DD.micro.
Created by Felipe Ferreira da Silva.

Usage:
  randomfasta [1] [2] [3] [4] [5] [6]

  1: Path to output file.
  2: Total of sequences (must be at least 1).
  3: Length of the sequences (must be at least 1).
  4: Randomness seed (must be at least 1).
  5: Units distribution (must contain at least 1 character).
  6: Show progress (0 for no, 1 for yes).
```

For example, executing `randomfasta out.fasta 1000 300 1234 ACCGGGT 1` will generate a file `out.fasta` containing 1000 sequences of length 300, and with the randomness seed 1234 the sequences will randomnly contain the characters `A`, `C`, `G` and `T`, with their chances of being selected based on the number of times they appear on `ACCGGGT`. The application will output the progress because the final argument is `1`. The character `G` will have a higher chances of appearing in the sequences than the character `C`, and the character `C` will have higher chances of appearing in the sequences than the characters `A` and `T`.

## License

Copyright (c) 2019 Felipe Ferreira da Silva

This software is provided 'as-is', without any express or implied warranty. In no event will the authors be held liable for any damages arising from the use of this software.

Permission is granted to anyone to use this software for any purpose, including commercial applications, and to alter it and redistribute it freely, subject to the following restrictions:

1. The origin of this software must not be misrepresented; you must not claim that you wrote the original software. If you use this software in a product, an acknowledgment in the product documentation would be appreciated but is not required.
2. Altered source versions must be plainly marked as such, and must not be misrepresented as being the original software.
3. This notice may not be removed or altered from any source distribution.
