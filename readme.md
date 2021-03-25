# Java网络编程系统学习
> 参考资料：《Netty权威指南》
## NIO入门
### BIO
- 为每个客户端连接创建一个新的线程
- 客户端个数:IO线程数 = 1:1
- 同步阻塞
### 伪异步IO
- 使用线程池
- 客户端个数:IO线程数 = M:N（M>>N）
- 同步阻塞
### NIO
- Selector 多路复用器（选择器）
- 客户端个数:IO线程数 = M:1
- 同步非阻塞
### AIO
- NIO2.0新增异步套接字通道
- 异步非阻塞
- 客户端个数:IO线程数 = M:0 （不需要额外的IO线程，被动回调）