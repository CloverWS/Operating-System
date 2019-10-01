# 操作系统 Operating System


清华大学OS课程: （内涵配套习题）https://github.com/chyyuu/os_course_info

哔哩哔哩网上课程：https://www.bilibili.com/video/av6538245?from=search&seid=2108582505794172756

## 目录

<!--ts-->
   * [目录](#目录)
   * [知识框架](#知识框架)
   * [进程与线程](#进程与线程)
   * [调度算法](#调度算法)
   * [同步](#同步)
   * [死锁](#死锁)
   * [进程间的通信](#进程间的通信)
   * [物理内存管理](#物理内存管理)
   * [同步虚拟存储](#虚拟存储)
   * [未完待续01.10.2019](#未完待续01.10.2019)
<!--te-->


---

## 知识框架

![](https://i.imgur.com/VfMIVxa.png)



---
## 进程与线程：
对应课件：2019春季OS课课件，第十一讲 进程与线程


进程的概念，特点及结构特征
![](https://i.imgur.com/tcRwfIf.png)
来源：http://www.kamow.top/c/%E8%BF%9B%E7%A8%8B%E7%9A%84%E7%89%B9%E7%82%B9

进程与程序的联系和区别（考点）
![](https://i.imgur.com/Xvr4guJ.png)
![](https://i.imgur.com/MU4G1eI.png)

进程的组成
![](https://i.imgur.com/KddVOJf.png)


进程控制块概念
![](https://i.imgur.com/eckdH9m.png)

进程的生命周期
![](https://i.imgur.com/MyvtEQq.png)

进程的挂起
![](https://i.imgur.com/FCLdtgC.png)


线程的概念
![](https://i.imgur.com/Om7wpAp.png)

线程的优缺点
![](https://i.imgur.com/TTWRaFJ.png)

与进程比较
![](https://i.imgur.com/kxdGG3t.png)

习题
![](https://i.imgur.com/mkXsd9p.png)
![](https://i.imgur.com/ZQ4ZCuC.png)
***必须理解掌握fork()，pthread_create(),pthread_jion()的原理和各个参数的意义！！！

Copy on write（必须掌握）
![](https://i.imgur.com/axRsuYd.png)
关于COW非常棒的文章：https://juejin.im/post/5bd96bcaf265da396b72f855

---

## 调度算法
![](https://i.imgur.com/PZ8pWOp.jpg)
![](https://i.imgur.com/73J0Z3L.jpg)

![](https://i.imgur.com/ODAh9Ot.jpg)

习题：
![](https://i.imgur.com/YXHHAeB.png)

调度算法：https://blog.csdn.net/xieminyao123/article/details/79116985
各种调度算法优缺点：https://blog.csdn.net/ttyue_123/article/details/52166497
调度算法模拟器：
https://ess.cs.tu-dortmund.de/Software/AnimOS/CPU-Scheduling/


---

## 同步
遗漏知识点很多，还未贯通

---

## 死锁（重点考点）

- 什么是死锁？

![](https://i.imgur.com/PrTsIQv.png)

- 死锁的四个必要条件
![](https://i.imgur.com/y5O8AmD.png)

- 资源分类
![](https://i.imgur.com/2abMI0X.png)

- 死锁的抽象图（没有完全理解）（考点-会画！）
![](https://i.imgur.com/3jkwGb7.png)
![](https://i.imgur.com/Wnidz2p.png)

- 资源占有图（考点-会画！）
![](https://i.imgur.com/g0tPxsP.png)
![](https://i.imgur.com/rJGwDwm.png)

- 进程预防
![](https://i.imgur.com/lFsiCZl.png)

- 进程避免
![](https://i.imgur.com/OwMYBvK.png)

- 进程检测
![](https://i.imgur.com/fMIWjGi.png)

- 进程处理
![](https://i.imgur.com/QyVRIOk.png)

- 竞争条件
![](https://i.imgur.com/rghLHlv.png)

- 习题
![](https://i.imgur.com/1ScdCPS.png)
![](https://i.imgur.com/pdkORW2.png)
- 经典问题
https://www.bilibili.com/video/av6538245/?p=68




---

## 进程间的通信
- 概念
![](https://i.imgur.com/4j9xhct.png)

- 信号，管道和消息队列
![](https://i.imgur.com/O2LHW2e.jpg)


---

## 物理内存管理
### 内部碎片和外部碎片
![](https://i.imgur.com/mJXz1bC.jpg)
https://blog.csdn.net/qq_22238021/article/details/80209062

### 非连续物理内存分配
https://yuerer.com/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F%E4%B9%8B-%E7%89%A9%E7%90%86%E5%86%85%E5%AD%98%E7%AE%A1%E7%90%86-%E9%9D%9E%E8%BF%9E%E7%BB%AD%E5%86%85%E5%AD%98%E5%88%86%E9%85%8D/
- 目的
![](https://i.imgur.com/qNFULjK.png)
- 实现
![](https://i.imgur.com/hvztaW0.png)
- 段式（习题）
![](https://i.imgur.com/9mPA7XS.png)
- 页式
![](https://i.imgur.com/C7DcImf.png)

### 连续物理内存分配
https://yuerer.com/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F%E4%B9%8B-%E7%89%A9%E7%90%86%E5%86%85%E5%AD%98%E7%AE%A1%E7%90%86-%E8%BF%9E%E7%BB%AD%E5%86%85%E5%AD%98%E5%88%86%E9%85%8D/
- Frist Fit, Best Fit, Worst Fit
![](https://i.imgur.com/6HXxaKE.jpg)
- 伙伴算法Buddy（必考！）
![](https://i.imgur.com/tCCBJBd.png)
![](https://i.imgur.com/6DPW1LE.png)
![](https://i.imgur.com/X0jkD1v.png)
![](https://i.imgur.com/aKFjBZt.png)

### 连续分配方式
- 单一，固定分区分配
https://blog.csdn.net/dongyanxia1000/article/details/51674627
- 动态分区分配
https://blog.csdn.net/dongyanxia1000/article/details/51700179
- 可重定位分配
https://blog.csdn.net/dongyanxia1000/article/details/51705957

---

## 虚拟存储
- 请求调页（去课件上看）
![](https://i.imgur.com/M8TWc3u.png)
![](https://i.imgur.com/uFOQKks.png)

### 页面替换算法
- FIFO
![](https://i.imgur.com/ydH2HAK.png)
- 最远优先
![](https://i.imgur.com/C2Jg6Y6.png)
- LRU
![](https://i.imgur.com/aAkWaL3.png)
- Clock
![](https://i.imgur.com/g6nyvPi.png)
![](https://i.imgur.com/ITedNn6.png)

- 抖动
![](https://i.imgur.com/ssR9VID.jpg)


## 未完待续01.10.2019
