> 2020 年下半年转 golang 开发。现在觉得多少有所成长，但总觉还是不够，所以，感觉是时候记录学习路上的一些点滴了。

# The road of being a good gopher

## 1. why
...
## 2. what
...
## 3. how
...
## 4. plan
...
## 5. leaning logs
### fatal error: concurrent map writes 
> 初学者可能都碰到过这个问题
<img width="315" alt="image" src="https://user-images.githubusercontent.com/3191641/159953881-4da4f06a-4054-4170-be39-a70c20f3583e.png">
<img width="666" alt="image" src="https://user-images.githubusercontent.com/3191641/159953135-21485b79-6616-4399-9f5b-10af7d4ea40d.png">

> 解决1: 写同一个 map 的地方都加锁
<img width="666" alt="image" src="https://user-images.githubusercontent.com/3191641/159953195-1c02bc1f-b7b5-47dd-81a5-9e252f734076.png">

> 解决2: sync.Map
了解说 `sync.Map` 在读多写少性能比较好，否则并发性能很差

