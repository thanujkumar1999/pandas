from asv_bench.benchmarks.frame_methods import *

self5 = Fillna()
self5.setup(False, 'pad', 'object')

%timeit self5.time_frame_fillna(False, 'pad', 'object')
191 ms ± 5.41 ms per loop (mean ± std. dev. of 7 runs, 1 loop each)  # <- master
127 ms ± 5.03 ms per loop (mean ± std. dev. of 7 runs, 10 loops each)  # <- PR
