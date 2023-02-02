### Task description

Parallel version of the [Conway's Game Of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life).

To reach that, field was splitted along Y-axis into some blocks of layers. Each block was given to specific MPI process, whose would calculate the next iteration of the block.

### Compilation

Program was compiled using this command:

```
mpicxx -std=c++11 -O3 ./src/main.cpp -o a.out
```
