# xv6-riscv-labs 计划书

按 6.S081 的实验顺序推进，完成一个记录一个。实验做完后，把实现内容和难点补进 [README](./README.md) 的对应章节。

## 待完成事项

- [ ] util — sleep、pingpong、primes、find、xargs
- [ ] syscall — trace、sysinfo
- [ ] pgtbl — 加速系统调用（USYSCALL）、打印页表、检测被访问的页
- [ ] traps — RISC-V 汇编、backtrace、alarm
- [ ] cow — 实现写时复制的 fork
- [ ] thread — Uthread、使用线程（哈希表加锁）、barrier
- [ ] net — 实现 e1000 网卡的收发
- [ ] lock — 内存分配器、块缓存加锁优化
- [ ] fs — 大文件、符号链接
- [ ] mmap — 实现 mmap 与 munmap
