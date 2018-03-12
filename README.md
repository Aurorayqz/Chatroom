# Chatroom
- 该项目实现了一个简单的聊天室，聊天室分为服务端和客户端。
- 该项目不涉及线程池、多线程编程、超时重传、确认收包等。

## 项目介绍
- 支持多个用户接入，实现聊天室的基本功能
- 使用epoll机制实现并发，增加效率
- 使用fork创建两个进程
- 将聊天信息写到管道（pipe），并发送给父进程
- 使用epoll机制接受服务端发来的信息，并显示给用户，使用户看到其他用户的聊天信息

## 编译

```
g++ server.cpp utility.h -o server
g++ client.cpp utility.h -o client
```

## 运行效果截图
- 实现了一个聊天室，在开启服务端后，用户可以连接服务器，加入聊天室（可开启多个client）
![server](https://github.com/Aurorayqz/Chatroom/blob/master/server.png)
![clien1](https://github.com/Aurorayqz/Chatroom/blob/master/client5.png)
![clien2](https://github.com/Aurorayqz/Chatroom/blob/master/client6.png)

