# matrix-f32-array-performace-issue

关于矩阵运算使用 FloatArray 作为存储的性能测试 demo.

> 第一次 loop 1000 (测初始性能)\
> 第二次 loop 1000000 (测 Turbo Fan 后性能)\
> 第二次 loop 10000 (测 Turbo Fan 后性能是否能保持)

[Online Test Link](https://deepkolos.github.io/matrix-f32-array-performace-issue/)

### Multiply&Invert

matrix_f32_array_issue_benchmark_1000_multiply&invert:

| Key                  | Value           |
| -------------------- | --------------- |
| three_no_f32_array   | 2.90ms (x2.071) |
| three_with_f32_array | 2.40ms (x1.714) |
| oasis_no_f32_array   | 1.40ms (x1.000) |
| oasis_with_f32_array | 2.10ms (x1.500) |

matrix_f32_array_issue_benchmark_1000000_multiply&invert:

| Key                  | Value            |
| -------------------- | ---------------- |
| three_no_f32_array   | 52.20ms (x1.000) |
| three_with_f32_array | 94.20ms (x1.805) |
| oasis_no_f32_array   | 61.70ms (x1.182) |
| oasis_with_f32_array | 67.10ms (x1.285) |

matrix_f32_array_issue_benchmark_10000_multiply&invert:

| Key                  | Value           |
| -------------------- | --------------- |
| three_no_f32_array   | 0.50ms (x1.000) |
| three_with_f32_array | 0.90ms (x1.800) |
| oasis_no_f32_array   | 0.60ms (x1.200) |
| oasis_with_f32_array | 0.60ms (x1.200) |

### Invert

matrix_f32_array_issue_benchmark_1000_invert:

| Key                  | Value           |
| -------------------- | --------------- |
| three_no_f32_array   | 4.60ms (x3.067) |
| three_with_f32_array | 3.20ms (x2.133) |
| oasis_no_f32_array   | 1.70ms (x1.133) |
| oasis_with_f32_array | 1.50ms (x1.000) |

matrix_f32_array_issue_benchmark_1000000_invert:

| Key                  | Value            |
| -------------------- | ---------------- |
| three_no_f32_array   | 44.80ms (x1.280) |
| three_with_f32_array | 49.90ms (x1.426) |
| oasis_no_f32_array   | 35.00ms (x1.000) |
| oasis_with_f32_array | 41.50ms (x1.186) |

matrix_f32_array_issue_benchmark_10000_invert:

| Key                  | Value           |
| -------------------- | --------------- |
| three_no_f32_array   | 0.50ms (x1.667) |
| three_with_f32_array | 0.50ms (x1.667) |
| oasis_no_f32_array   | 0.30ms (x1.000) |
| oasis_with_f32_array | 0.40ms (x1.333) |

### Multiply

matrix_f32_array_issue_benchmark_1000_multiply:

| Key                  | Value           |
| -------------------- | --------------- |
| three_no_f32_array   | 2.00ms (x1.250) |
| three_with_f32_array | 2.10ms (x1.312) |
| oasis_no_f32_array   | 1.60ms (x1.000) |
| oasis_with_f32_array | 1.80ms (x1.125) |

matrix_f32_array_issue_benchmark_1000000_multiply:

| Key                  | Value            |
| -------------------- | ---------------- |
| three_no_f32_array   | 30.30ms (x1.000) |
| three_with_f32_array | 50.10ms (x1.653) |
| oasis_no_f32_array   | 42.40ms (x1.399) |
| oasis_with_f32_array | 49.10ms (x1.620) |

matrix_f32_array_issue_benchmark_10000_multiply:

| Key                  | Value           |
| -------------------- | --------------- |
| three_no_f32_array   | 0.30ms (x1.000) |
| three_with_f32_array | 0.50ms (x1.667) |
| oasis_no_f32_array   | 0.40ms (x1.333) |
| oasis_with_f32_array | 0.50ms (x1.667) |

### 相关 Links

https://github.com/toji/gl-matrix/issues/359
https://github.com/akira-cn/babel-plugin-transform-gl-matrix/blob/master/README-CN.md
