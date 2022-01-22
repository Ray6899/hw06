## 实验结果
除了saxpy和scanner之外，其余函数都有明显的速度提升

```
fill: 0.59706s
fill: 0.607065s
fill_parallel: 0.134176s
fill_parallel: 0.13482s
saxpy: 0.0321525s
saxpy_parallel: 0.031659s
sqrtdot: 0.0801601s
5165.4
sqrtdot_parallel: 0.0160526s
5792.62
minvalue: 0.0724999s
-1.11803
minvalue_parallel: 0.0109034s
-1.11803
magicfilter: 0.272147s
55924034
magicfilter_parallel: 0.164996s
55924034
scanner: 0.0879465s
6.18926e+07
scanner_patallel: 0.132198s
6.18926e+07
```

## 完成情况
- fill ：使用tbb parallel for
- saxpy：依旧使用tbb parallel for
- sqrtdot：使用tbb parallel reduce
- minvalue：使用tbb parallel reuce
- magicfilter: 使用tbb parallel for 和 锁实现
- scanner：使用tbb parallel scan实现