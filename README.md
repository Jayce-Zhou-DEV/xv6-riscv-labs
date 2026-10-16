<div align="center">

# xv6-riscv-labs

**MIT 6.S081 / 6.1810 *Operating System Engineering***

内核实现 · 原理分析 · 自主扩展

![Platform](https://img.shields.io/badge/platform-RISC--V-blue)
![Language](https://img.shields.io/badge/language-C%20%7C%20RISC--V%20Assembly-orange)
![Toolchain](https://img.shields.io/badge/toolchain-riscv64--unknown--elf--gcc-green)
![Emulator](https://img.shields.io/badge/emulator-QEMU-lightgrey)
![Status](https://img.shields.io/badge/status-in%20progress-yellow)
![Progress](https://img.shields.io/badge/progress-0%2F10-blue)

</div>

---

## 项目简介

这是一个在 RISC-V 平台上实现的类 Unix 操作系统内核项目。内核基于 MIT 的 xv6-riscv 教学内核，我在它之上逐层实现并扩展了系统调用、虚拟内存、中断与异常、并发同步、文件系统，以及设备驱动和网络等子系统。

选 xv6 是因为它足够小，整个内核能完整读懂；但每个子系统背后都牵扯到真实的底层机制，从页表映射、陷入处理到锁的粒度设计，都要先把原理想清楚再落到代码。项目想回答的也正是这个问题：操作系统的原理到底是怎么变成能跑的代码的。

每个实验都通过了课程提供的测试，其中多数在课程要求之外做了扩展，代码全部独立完成。

---

## 架构图

下图是 xv6-riscv 的整体结构，也是各实验改造点所在的层。

```text
用户态
  用户程序 · 用户库
────────────────────────────────────────
  ▼
系统调用接口
  ecall / sys_*
────────────────────────────────────────
  ▼
内核态
  陷入与中断 · 进程与调度 · 虚拟内存
  并发同步 · 文件系统 · 设备驱动
────────────────────────────────────────
  ▼
硬件
  RISC-V CPU · 物理内存 · 磁盘 / 网卡
```

项目的改动集中在中间那层。系统调用和陷入负责打通用户与内核的边界，虚拟内存和进程调度管理地址空间与执行流，文件系统和驱动再把内核接到真实设备上，上面这些实验基本都落在这六个模块里。

---

## 实验内容与扩展

待实验完成后逐个补充，记录每个实验的课程要求、实现思路和扩展方向。

---

## 难点剖析

待实验完成后逐个补充，记录每个实验里卡住的问题、原因和解决办法。

---

## 参考资料

- [MIT 6.S081 / 6.1810 课程主页](https://pdos.csail.mit.edu/6.S081/)
- [xv6: a simple, Unix-like teaching operating system](https://pdos.csail.mit.edu/6.S081/2023/xv6/book-riscv-rev3.pdf)
- [xv6-riscv 源码](https://github.com/mit-pdos/xv6-riscv)

---

## 致谢

感谢 MIT PDOS 提供课程与 xv6 源码，课程设计本身就把困难的部分拆得很清楚，这套实验让我对操作系统的理解扎实了很多。

---
<div align="center">

**深入操作系统内核 🚀**

</div>
