##### netio

-  只有非阻塞的socket支持ET模式
-  ET模式下，循环读取数据，知道read返回-1，此时errno是EWOULDBLOCK
-  ET模式下，写入数据，当对方缓存不够时，也是返回-1，errno是此时errno是EWOULDBLOCK
