# retrofit
source code for retrofit

## Usage

You can run generate.py to create a set of executables to run the experiments based on core.h, which contains the core algorithm of retrofit and compared algorithms.

Either Monte Carlo or a memory trace can be used to simulate. The Monte Carlo parameters can be modified within the generate.py file.

# Config

| Parameter | Description | Suitable Algorithm |
| --- | --- | --- |
| xxx.high | count of cols or rows with high probability in one period (xxx can be row_rand of col_rand) | all |
| xxx.low | count of cols or rows with low probability in one period (xxx can be row_rand of col_rand) | all |
| xxx.times | num of periods of row (xxx can be row_rand of col_rand) | all |
| xxx.percent | probalibity that the write falls on high probability rows or cols (xxx can be row_rand of col_rand) | all |
| swap_endurance | the endurance used while the wear-leveling swap bits | all but uniform |
| mean | mean of the normal distribution of the memory endurance | all |
| cov | covirance of the normal distribution of the memory endurance | all |
| row_swap_interval | how many writes are simulated every time the algorithm swaps the row | start_gap, ars |
| col_swap_interval | how many writes are simulated every time the algorithm swaps the col | ilf, byte rotation, counter_cw |
| extra_row | how many gaps (usually) are used in the method | retrofit |
| retrofit_times_m | average swap interval | retrofit |
| retrofit_times_m | swap interval for error gaps | retrofit |
| swap_counts | how many rows are swapping each time | ars |
| global_pointer_count | how many global pointers are produced by retiring a row | retrofit |
| group_bits | how many bits per group | counter_cw, hwl |

# Flags

| Flag | Description |
| --- | --- |
| ecp0, ecp1, ... | error correction pointer count |
| ecc | error correction code used instead of ecpx |
| uniform | the memory write pattern is uniform |
