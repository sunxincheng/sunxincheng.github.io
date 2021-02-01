---
title: Thread 进程
date: 2020-05-07 21:47:05
tags:
---
#　进程资源函数 (resource limit)
 
``` C
#define RLIMIT_CPU                   0                    /* CPU time in ms */
#define RLIMIT_FSIZE                 1                    /* Maximum filesize */
#define RLIMIT_DATA                  2                    /* max data size */
#define RLIMIT_STACK                 3                    /* max stack size */
#define RLIMIT_CORE                  4                    /* max core file size */
#define RLIMIT_RSS                   5                    /* max resident set size */
#define RLIMIT_NOFILE                6                    /* max number of open files */
#define RLIMIT_AS                    7                    /* address space limit(?) */
#define RLIMIT_NPROC                 8                    /* max number of processes */
#define RLIMIT_MEMLOCK               9                    /* max locked-in-memory address space */
#define RLIMIT_LOCKS                 10                   /* maximum file locks held */
#define RLIMIT_SIGPENDING            11                   /* max number of pending signals */
#define RLIMIT_MSGQUEUE              12                   /* maximum bytes in POSIX mqueues */

#define RLIM_NLIMITS                 13
```
rlim_cur字段是资源的当前资源限制，例如current->signal->rlim[RLIMIT_CPU],rmlim_cur表示正在运行进程所占用的CPU时间的当前限制。
# 进程切换（process switch）
硬件上下文-->进程恢复执行前必须装入寄存器的一组数据称为硬件上下文