# Benchmark
There are two useful functions to measure how long things take:

`get_time()` returns the time in seconds since the start of the game.

`get_op_count()` returns the number of operations performed since the start of execution.

Most actions take a constant number of operations, and as long as the speed factor remains the same, the time per operation is also constant.

Actions that do not affect the drone, such as reading variables and calling functions all count as `1` operation. (Calling a function usually consists of reading out the function from a variable and then calling it, so it's `2` operations)

Drone actions like planting, harvesting or moving count as `200` operations.


Note that performance in the real world is much more complex than this. Consistent op counts like this are a simplification made for this game.