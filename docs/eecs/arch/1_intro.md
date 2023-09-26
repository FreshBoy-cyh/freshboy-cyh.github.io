# Chapter 1: Introduction

每次硬件课开头都要集中讲一堆概念，还有好多重复的，反正[计组开头](https://xuan-insr.github.io/computer_organization/1_prelude/)介绍过的概念这边就不写了。

Quantitative Approaches：

* Latency (Response Time) - 从开始到结束的时间是多少
* Throughput - 在给定的时间内所做的工作量是多少
* Elapsed Time - 总的响应时间，包括所有方面的处理（I/O, OS开销，空闲时间）
* CPU Time - 处理给定作业所花费的时间
* MIPS - Millions of Instructions per Second，描述处理器性能的单位，只能比较 ISA 相同的 CPU

Flynn's Taxonomy: A classification of computer arch based on the number of streams of instructions and data，名词解释见[此文章](https://zhuanlan.zhihu.com/p/27696267)。

Dependability（可靠性）这个概念是故意设得很空泛的，相关的量化指标有：

* MTTF: Mean Time To Failure
* MTTR: Mean Time To Repair
* FIT : Failure In Time = 1 / MTTF
* MTBF: Mean Time Between Failure = MTTF+MTTR
* Module Availability= MTTF / (MTTF + MTTR)
