## Cuda Implementation of Parallel Prefix Sum (Blelloch Scan)

### References
[http://http.developer.nvidia.com/GPUGems3/gpugems3_ch39.html]
[https://www.cs.cmu.edu/~blelloch/papers/Ble93.pdf]


### Sample Output

```
$ nvcc -o psum psum.cu      # nvcc compile
$ ./psum                    # run
0  0
3  0
6  3
9  9
12  18
15  30
18  45
21  63
24  84
27  108
...
...
...
2970  1468665
2973  1471635
2976  1474608
2979  1477584
2982  1480563
2985  1483545
2988  1486530
2991  1489518
2994  1492509
2997  1495503

# quick check
$ python2 -c 'print sum(range(0, 3000, 3)) - 2997'
1495503
```
