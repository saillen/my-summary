# netstat 及 TCP 相关状态研究

- LISTEN：      侦听来自远方的TCP端口的连接请求
- SYN-SENT：    再发送连接请求后等待匹配的连接请求
- SYN-RECEIVED：再收到和发送一个连接请求后等待对方对连接请求的确认
- ESTABLISHED： 连接建立
- FIN-WAIT-1：  等待远程TCP连接中断请求，或先前的连接中断请求的确认
- FIN-WAIT-2：  从远程TCP等待连接中断请求
- CLOSE-WAIT：  等待从本地用户发来的连接中断请求
- CLOSING：     等待远程TCP对连接中断的确认
- LAST-ACK：    等待原来的发向远程TCP的连接中断请求的确认
- TIME-WAIT：   等待足够的时间以确保远程TCP接收到连接中断请求的确认
- CLOSED：      连接关闭
