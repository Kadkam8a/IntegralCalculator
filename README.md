# Integral Calculator
Second practice of High Performance Computing at National [Autonomus University of Mexico](https://www.unam.mx/) (2023-2)


Karime Ochoa Jacinto ([Kadkam8a](https://github.com/Kadkam8a))

GNU/GPL License 3.0

## Project description

Parallel computing allows us to segment a determinate task into small pieces to distribute them between processors in order to make the process faster. 

The present project (a modification of the one made in class) calculates the Riemann integral of $x^2$ with a barber algorithm as follows:
1. The user determines the values for: 
    - $a$: lower end of interval. 
    - $b$: upper end of interval.
    - $segments$: number of segments in wich the interval will be divided. 
    - $n$ _ $partitions$: number of step sizes in wich each segment will be divided (the precision increases as this number does).
2. The program calculates the size of $dx$ and $block$.
3. Each procesor calculate the integral of a segment
4. The master procesor adds the results.

This image shows a visual representation of the meaning of the variables used.


![](https://github.com/Kadkam8a/IntegralCalculator/blob/main/variables.png)
## Running and compilation
To compile the program you have to type on the terminal:
```
mpicc \-o name main.c
```
To run the code 
```
mpiexec -n 4 ./try a b segments n_partitions
```
## Example
For this example the inputs were:
```
mpiexec -n 4 ./try 0 2 5 4000
```
![](https://github.com/Kadkam8a/IntegralCalculator/blob/main/ejemplo.png)
## Used tools
- [MPICH](https://www.mpich.org/).
## References
- Wikipedia (2023). *MPICH*. Retrieved in 30.05.2023 from [https://en.wikipedia.org/wiki/Ptolemy](https://en.wikipedia.org/wiki/MPICH)
