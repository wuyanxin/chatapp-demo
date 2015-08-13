文章：[http://www.jianshu.com/p/40d8bc17529f](http://www.jianshu.com/p/40d8bc17529f)

### 多房间聊天
socket.io提供[rooms和namespace的API](http://socket.io/docs/rooms-and-namespaces/)
用rooms的API就可以实现多房间聊天了，总结出来无外乎就是：join/leave room 和 say to room
```
// join和leave
io.on('connection', function(socket){
  socket.join('some room');
  // socket.leave('some room');
});

// say to room
io.to('some room').emit('some event'):
io.in('some room').emit('some event'):
```


###### 运行效果
![运行效果](http://upload-images.jianshu.io/upload_images/436630-d01d00f22a54a6e3.png?imageMogr2/auto-orient/strip|imageView2/2/w/1240)

