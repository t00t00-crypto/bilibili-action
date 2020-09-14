# 哔哩哔哩直播自动签到
> 哔哩哔哩直播自动签到

## Github Actions 部署指南

### 一、Fork 此仓库
![image-20200727142541791](https://i.loli.net/2020/07/27/jK5H8FLvt7aBeYX.png)



### 二、设置账号COOKIE
先登录B站，然后访问https://api.live.bilibili.com/sign/GetSignInfo，按***F12***，在***Network***中刷新

![image-20200727150526051](https://i.loli.net/2020/07/27/zSFRqjIr4B8OEgh.png)

复制***cookie***中的内容，从***sid***开始至***infoc***（可能有所不同）



在***GitHub***中添加名为 **COOKIE**的变量，值为复制的内容。

> Settings-->Secrets-->New secret

支持多账号，账号**COOKIE**之间用 ***#*** 分隔

示例：**COOKIE:sid=97d0....#sid=97d0....**
![image-20200727142753175](https://i.loli.net/2020/07/27/xjri3p4qdchaf2G.png)

### 三、启用 Action
1. 点击 ***Actions***，再点击 **I understand my workflows, go ahead and enable them**

   ![](https://i.loli.net/2020/07/27/pyQmdMHrOIz4x2f.png)

2. 点击左侧的 ***Star***

   ![image-20200727142617807](https://i.loli.net/2020/07/27/3cXnHYIbOxfQDZh.png)

### 四、查看运行结果
> Actions --> 签到 --> build
>
> 能看到如下图所示，表示成功

![](https://i.loli.net/2020/07/27/YLkpXSbRj73nwov.png)

## 注意事项

1. 每天运行两次，在上午 6 点和晚上 22 点。

2. 可以通过 ***Star*** 手动启动一次。

   ![image-20200727142617807](https://i.loli.net/2020/07/27/87oQeLJOlZvU3Ep.png)
   
   
