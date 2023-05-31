# Integral Calculator

National Autonomous University of Mexico (https://www.unam.mx/).
Karime Ochoa Jacinto ([Kadkam8a](https://github.com/Kadkam8a))

## License

Copyright © 2023 <karime8aj@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Project description

Parallel computing allows us to segment a determinate task into small pieces to distribute them between processors in order to make the process faster. 

The present project calculates the Riemann integral of $x^2$ with a barber algorithm as follows:
1. The user determines the values for: 
    - $a$ :lower end of interval. 
    - $b$ : upper end of interval.
    - $segments$ :number of segments in wich the interval will be divided. 
    - $n$ _ $partitions$ :number of step sizes in wich each segment will be divided (the precision increases as this number does).
2. The program calculates the size of $dx$ and $block$.
3. Each procesor calculate the integral of a segment
4. The master procesor adds the results.

This image shows a visual representation of the meaning of the variables used.


To compile the program you have to type on the terminal:
```
mpicc \-o name main.c
```
To run the code 
```
mpiexec -n 4 ./try a b segments n_partitions
```

## Example
## Used tools
- [MPICH](https://www.mpich.org/).
## References
- Wikipedia (2023). *MPICH*. Retrieved in 30.05.2023 from [https://en.wikipedia.org/wiki/Ptolemy](https://en.wikipedia.org/wiki/MPICH)
