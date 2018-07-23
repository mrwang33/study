**JVM学习**

- 内存模型![内存模型](https://i.loli.net/2018/07/23/5b558d3b34e89.png){:height="200px" width="200px"}
- 运行时数据区![运行时数据区](https://i.loli.net/2018/07/23/5b558d4313bab.png){:height="200px" width="200px"}

- 程序计数器: 指向当前线程正在执行的字节码指令的地址和行号
每个线程都有一个属于自己的程序计数器

- 虚拟机栈 存储当前线程运行方法所需要的数据、指令和返回地址

- 将class文件转成汇编代码 javap -c -v xxxx.class > p.txt